# coder packaging Instructions

## Table of Contents

> Anywhere you see/hear **SpringWise** in the _documentation_ or _video_, think "**cp**"

1. [Starting cp](#1-starting-cp)

    - [Instructional Video: Starting cp](#-starting-cp-instructional-video)

2. [Setting Up cp](#2-setting-up-cp)

---

## Must Have's Before Getting Set-Up

1. **Java JDK 17** in your IDE/IDEA. If you don't, the **cp** app will not run.
2. Eclipse IDE users need **Eclipse 2021-09 (4.21)** or later. If you don't, please install a newer version.

## Starting cp

---

### 1. GitHub

<details>
<summary>What is GitHub?</summary>

> - GitHub is a web-based platform used for version control and collaboration on software development projects.
> - Think of it as a very cool online storage location where you can safely store your code to share with yourself or
    others.
    >
- You can have as many versions/iterations of your code as you'd like.
>  - In case you accidentally delete your code/project on your computer, it's good to have your code safely on GitHub,
     so you can safely retrieve it whenever you like.
---
</details>

1. Be given access to contribute too https://github.com/CodersCampus/cp, private repository via (Pete).
2. Click on green `<> Clone` button.
3. Click `Open with GitHub Desktop`.
4. Browser will display pop up window `Open GitHub Desktop.app?`.
5. Click `Open GitHub Desktop.app` button.

### 2. GitHub Dektop

<details>
<summary>What is GitHub Desktop?</summary>

> - At the most basic level, GitHub Desktop is an application that allows us to grab projects from GitHub and store them
    onto our computer.
    >
- GitHub Desktop handles a lot of technical features under the hood.
---
</details>

6. In GitHub Desktop, **Clone a Repository** window opens to the **URL** tab.
7. Keep the _**Repository URL or GitHub username and repository**_ field as is.
8. You can keep the _**Local Path**_ as is or change it by pressing the `Choose` button and selecting a different
   location in Finder/Explorer to store the cp repository.
9. Next, click blue `Clone` button.
10. **Current Repository** should be `cp`, **Current Branch** should be `dev`, and you'll have the option
    to `Fetch origin`.

<img style="border-radius: 10px" width="550" alt="GitHub Desktop default" src="images/1_gitHubDesktop.png">

### 3. Opening cp

<details>
<summary>What is cp?</summary>

> - cp, aka **coder packaging**, is our in house application that we are building out as a team.
    >
- The app started with a handful of Coders Campus wanting to build an application that utilized what we were learning in
  the course.
>   - It is growing to become an application that the students are using daily to track their coding experience.
>   - From day one, this application is a teaching tool for students, designed to show us what the real world is like as
      a Software Engineer.
      >
- We learn how to work as a team, disagree and communicate as a team, and build something bigger than ourselves
  together.
---
</details>

11. Now open **cp** repository
12. If you are given the option in GitHub Desktop to `Open in Eclipse IDE...`, then click that button.

> If you do not see `Open in Eclipse IDE...`, you have the option of clicking on "Preferences" and updating the
> programming application you'd like to use.

<img style="border-radius: 10px" width="550" alt="Open with Eclipse IDE" src="images/2_openWithEclipseIDE.png">

13. If you do not see that option, then open **Eclipse IDE** app, click
    on `File` > `Open Projects from File System...` > `Directory` > locate **cp** root folder, and click `Open`.

<img style="border-radius: 10px" width="450" alt="cp root folder" src="images/3_cpRootFolder.png">

### 4. Eclipse IDE

<details>
<summary>What is Eclipse IDE</summary>

> - Eclipse IDE (Integrated Development Environment) is a development platform used primarily for Java development.
    >
- This is the programming application we'll use to code out our tasks, exercises and Assignments.
>   - Eclipse IDE is one of a few applications we use to code in.
      >
- We'd like you to get familiar with Eclipse IDE, before branching out to other platforms.

</details>

14. Eclipse will open and give you the prompt window "**Import Projects from File System or Archive**".
15. In the "**Import Source**" field, that should be left alone, as that's where you choose to store the **cp**
    repository, earlier in GitHub Desktop.
16. Click bottom right button `Finish`.
17. You may see "**Import as Maven project**", if you do, select **Maven**, as this is how you need to import this
    project.
18. **cp** should populate within the **Project Explorer** side panel of **Eclipse IDE**.

### 5. Run cp

19. To run **cp** application you will traverse through the **cp** folder structure clicking the dropdown arrows as you
    go.

- That path is, `cp/src/main/java/com.coderscampus/cpApplication.java`.
- Open `CPApplication.java`.
- Press the green `Run` button to run application or right click on main method of `CPApplication.java`, and
  select `Run As` > `Java Application`.

20. You should see the **Spring Boot** design in the console with a bunch of other content.

<img style="border-radius: 10px" width="600" alt="Running cp" src="images/4_runningCP.png">

21. Now navigate to browser of choice, we use Chrome, and type into the address bar `localhost:8080`, this is the local
    address the **cp** application is being served too.
22. **cp** application should be live on your browser.
23. If prompted to **Login**, then login to the application using a Gmail account.

---

### 📹 [Starting cp Instructional Video](https://youtu.be/N8m2b1AFvDo)

_- If you have any questions please follow up the team at Coder Campus for assistance_

---

## Setting up cp

To set up **cp** on your computer, follow these guidelines:

- Grab the `dev` branch via **GitHub Desktop** or **Terminal/BASH**
- Run it via **Eclipse IDE** or **IntelliJ IDEA**

> Choose the method you're most comfortable with to get **cp** operational.

### 1. Get cp `dev` branch

---

#### GitHub Desktop Instructions

1. Open **GitHub Desktop**
2. Ensure the **Current Repository** is `cp`, if not click the **Current Repository** drop-down and select the `cp`
   repository.
3. Ensure **Current Branch** is the `dev` branch.
4. Click `Fetch origin`.
5. If you see `Pull`, after pressing `Fetch origin`, then click `Pull`.
6. Open IDE of choice
    - If using **Eclipse IDE**, right click root `cp` folder and click **Refresh** if it's not already on `dev` branch.

<img style="border-radius: 10px" width="550" alt="GitHub Desktop screenshot instructions" src="images/5_runningWithGitHubDesktop.png">

---

#### Terminal/Git BASH Instructions

1. `cd` into **cp** project folder and type the following git commands into your Terminal/Git BASH
    - `git status` - provides info on the current state of the repo. Not required, just nice to info to have.
    - `git fetch` - retrieves the latest changes from a remote repository without merging them to the local branch.
    - `git pull` - performs a `git fetch` to update local repository with changes from the remote, then performs
      a `git merge` to merge any
      changes fetched into the current branch.

> _Performing a `git fetch` AND a `git pull` will mitigate potential issues, vs. just performing a `git pull`._

<img style="border-radius: 10px" width="450" alt="GitHub Desktop screenshot instructions" src="images/6_terminal.png">

2. Then open IDE of choice. Our go-to is **Eclipse IDE**.

### 2: Open cp and run locally

---

#### Run cp via Eclipse IDE

1. Navigate or open to **cp** application, inside of **Eclipse IDE**.
2. Right click on root folder of **cp** and click **Refresh**.
3. `[cp dev]` should appear to the right of your cp project.
4. Navigate to [localhost:8080](http://localhost:8080/) in your browser of choice, we suggest Google Chrome, and ensure
   it's running successfully.

<img style="border-radius: 10px" width="300" alt="GitHub Desktop screenshot instructions" src="images/7_eclipse.png">

> #### Eclipse Troubleshooting Steps
> **Solution:**
> 1. On the `pom.xml` file, `right click > Run As > Maven Clean`
> 2. `Run As > Maven Install`
>
> _If the Installation fails:_
> - **On Windows:** delete the h2 local database C:\Users\%user%\h2dataspringwise.mv
    >
- Repeat Solution 1, Steps 1 and 2.

#### Run cp via IntelliJ IDEA

1. Navigate or open the **cp** application, inside of **IntelliJ IDEA**.
2. Ensure that you see the **dev** branch selected.
3. Navigate to [localhost:8080](http://localhost:8080/) in your browser of choice, we suggest Google Chrome, and ensure
   it's running successfully.

<img style="border-radius: 10px" width="300" alt="GitHub Desktop screenshot instructions" src="images/8_intelliJ.png">

---

### Extras

If using Terminal/BASH here's the shortcut installation instructions for opening projects into VS Code

- [Open Project into VS Code via `code .` Command](VS_CODE_PATH_INSTRUCTIONS.md)

---

### Issues

Encounter any setup issues with **cp**? Please post your questions to the **#active-full-stack** Slack channel.














