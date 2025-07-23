# HOW TO MANUALLY SEED DATA

For your dev envirnment only, to allow you to do more serious manual testing.

This is very powerful but also breaks a ton of rules, so do this only on it's own profile and run it only on your own box.

You will need to be able to run this in two modalities:
  - one to create the data
  - another to destroy the data you created

Or you could also just delete your h2db at will, if you didn't want to create the second modality.

Either way _**"With great power comes great responsibility"**_

## Notes

### A “Spring‑y” way to run one‑off logic without touching your main web entry‑point

1. **Move the logic into a `CommandLineRunner` (or `ApplicationRunner`) bean.**
   That bean runs *after* the `ApplicationContext` is ready, so you have full DI (repositories, services, etc.).

2. **Guard the bean with a special Spring profile** (e.g. `seed`) so it fires only when you explicitly enable it.

3. **Launch the app in *CLI mode*** (`WebApplicationType.NONE`) from a second `main` class.
   That second entry point re‑uses your normal configuration but starts *without* the servlet container, executes the runner, and then exits.

---

#### 1  Your normal web application stays unchanged

```java
@SpringBootApplication
public class CPApplication {
    public static void main(String[] args) {
        SpringApplication.run(CPApplication.class, args);   // full web stack
    }
}
```

---

#### 2  A one‑off runner bean, active only in profile `seed`

```java
@Profile("seed")                 // run only when profile is enabled
@Component
@RequiredArgsConstructor
@Transactional
public class StudentSeeder implements CommandLineRunner {

    private final StudentRepository studentRepo;

    @Override
    public void run(String... args) {
        Student s1 = new Student("abc", "name1", 1, "IntelliJ", false, "mentor1", null);
        Student s2 = new Student("def", "name2", 2, "IntelliJ", false, "mentor2", null);
        studentRepo.saveAll(List.of(s1, s2));              // use your repo as usual

        /** YOU CAN CREATE HUNDREDS OF RECORDS 
         * in any and every table, right here, 
         * using the above type of code,  
         * CheckinServiceTest or any other that Robert has done,
         * for examples
         * */
    }
}
```

*Why a profile?* – It keeps the bean out of every normal launch, including CI/CD, tests, and prod.

---

#### 3  A dedicated CLI entry point

```java
public class SeedApplication {
    public static void main(String[] args) {
        // Re‑use all CPApplication configuration, but start in non‑web mode
        ConfigurableApplicationContext ctx =
            new SpringApplicationBuilder(CPApplication.class)
                    .profiles("seed")             // activates StudentSeeder
                    .web(WebApplicationType.NONE) // skips Tomcat/Jetty
                    .run(args);

        // Shut down gracefully after the runner finishes
        System.exit(SpringApplication.exit(ctx));
    }
}
```

Run it from your IDE or command line:

```bash
# from a built JAR
java -cp cp‑app.jar com.example.SeedApplication
```

or, without a second `main`, you can simply run:

```bash
java -jar cp‑app.jar \
     --spring.profiles.active=seed \
     --spring.main.web-application-type=none
```

Either way, only the `StudentSeeder` bean executes; the application quits immediately afterwards.

---

### Why this is considered canonical

| Concern                         | How this pattern addresses it                                        |
| ------------------------------- | -------------------------------------------------------------------- |
| **DI & transaction management** | Uses Spring‑managed beans rather than manual `new StudentRepoImpl()` |
| **No duplicate configuration**  | Re‑uses `CPApplication` context; nothing extra to wire               |
| **Non‑web launch**              | `WebApplicationType.NONE` avoids starting embedded Tomcat/Jetty      |
| **Predictable activation**      | Profile gating guarantees the code never runs unintentionally        |
| **Graceful shutdown**           | `SpringApplication.exit(ctx)` lets Spring close the context cleanly  |

---

#### Alternatives you might also consider

* **Flyway/Liquibase data migrations** – ideal for repeatable seed data that travels with every environment.
* **Spring Shell** – provides a rich CLI if you foresee many adhoc tasks.
* **`SpringApplication.from()` (Boot 3.x)** – an even terser way to reuse the primary `main`, e.g.:

  ```java
  SpringApplication
      .from(CPApplication::main)
      .with(StudentSeeder.class)  // add extra beans
      .web(WebApplicationType.NONE)
      .run(args);
  ```

For a simple developer‑only seeding job, though, the `CommandLineRunner + profile + CLI entry point` approach is the clean, idiomatic solution.
