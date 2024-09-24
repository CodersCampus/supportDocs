Here is a step-by-step guide to add a `.gitignore` file directly inside **GitHub Desktop**:

### Step 1: **Open Repository Settings**
1. Once the repository is created, *but before you commit & push the first time* **Go to the "Repository" menu** at the top and select **Repository Settings**.
2. In the **Repository Settings** window, click on the **Ignored Files** tab.
   - This is where you can add files and directories that you want Git to ignore.

### Step 4: **Add Entries to `.gitignore`**
1. In the **Ignored Files** tab, add the files, directories, or patterns you want Git to ignore.
   - For example, you should add:
     ```
     /bin/
     .classpath
     .project
     .DS_Store
     ```
2. Each line represents a different file, folder, or pattern to ignore.
3. Once you’re done adding the entries, click **Save**.

### Step 5: **Commit the `.gitignore` File**
1. After adding ignored files in the repository settings, **GitHub Desktop will automatically create a `.gitignore` file**.
2. In the **Changes** tab, you will see that a new `.gitignore` file has been created and listed as a change.
3. Enter a **commit message** (e.g., "Add .gitignore").
4. Click **Commit to master/main** to save the `.gitignore` file to the repository.

### Step 6: **Push Changes to GitHub**
1. After committing the `.gitignore` file, click **Push origin** to upload your changes to the remote repository on GitHub.

### Step 7: **Verify on GitHub**
1. Go to your repository on **GitHub.com**.
2. You should see the `.gitignore` file listed, and files added to `.gitignore` will no longer be tracked in the repository.

---

### Summary:
- **After you create a new repository** in GitHub Desktop.
- **Open repository settings** and add files to ignore directly through GitHub Desktop under **Ignored Files**.
- **Commit and push the `.gitignore`** without leaving GitHub Desktop.

## The following videos in the coursework cover GitIgnore:

### Unit 3-4 Java Basics:

Lesson 2: Quick Git Talk (git ignore starts at 2 min mark)

[Quick Git Talk](https://courses.coderscampus.com/students/courses/274/sections/675/lessons/4801)


### The BEST video is the Assignment GitHub Prep (start at 8 minute mark) 

After Lesson 10: 

[Assignment GitHub Prep](https://courses.coderscampus.com/students/courses/274/sections/675/lessons/4812)