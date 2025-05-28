# Assignment 14 Don't Use a Database… Unless You Do It Right! 

## TL;DR

If **session storage** or **in-memory data** fits the scope, go with that.  
In general, only bring in a database **if the project’s logic truly requires it**.

For **Assignment 14**, which focuses on **JavaScript** and **session storage**, a full database setup is **not required**, and definitely **should not save a User**.

Keep it light. Keep it smart. Build with purpose. 

---

## ❌ Real Example of What *Not* to Do

Let me show you why...

If your app saves each user to the database, you’ll quickly get duplicates.  
Why? Because each time a user refreshes the page, opens a new tab, or re-enters their name, the app creates a **new User record**.

There’s no session logic tying a user to a consistent ID, so the database just keeps adding more "Marys" (or "Larrys") even though it’s the same person.

👉 You see where this is going?

---

## ✅ What Actually Needs Saving?

If you’re not saving users, then what *should* you persist?

* **Messages**  
* **Channels** (optional)

Think back to Trevor’s video example from Assignment 14.

> Did he have more than one channel?

Nope — just `#general`.

So ask yourself:  
Is it worth spinning up full DB tables just for one channel?  
**Probably not.**

---

## 💭 But What If...?

Yeah, it *is* kind of fun to let users **create new channels**.

But even if you’re adding that feature, here’s the real question:

> If you're not saving **Users** *or* **Channels**...
> ...is it really worth setting up a whole MySQL database, extending JPA, designing entity relationships, and wiring up the back end **just to store messages**?

Even if it’s fun to add extra features, ask yourself:  
**Does the effort of a full DB setup really match what you’re saving?**

If you're just storing chat messages, in-memory storage or JSON may be all you need.

---

## ✅ When *Is* It Worth Using a Database?

If you’re planning to:

- Save and persist **users**
- Tie messages to authenticated users
- Allow custom, persistent **channels**
- Enable re-login or profile editing

…then yes — a real database makes sense.

Just be intentional and avoid the overkill when your app can run smoothly without it.

---

Big thanks to Kevin Gallaccio for the clarity on this! 🙌  
And yeah, it’s weird to learn SQL and then be told not to use it.  
But if you *do* decide to implement a database, **do it for the right reasons—and do it right**.

