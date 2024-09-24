# Structuring Your Project Repository

Theoretically, if your project is strictly private, then it is your own business what you do inside it.

This does not apply if you are asking others for assistance.

As soon as you ask others for help or turn in an assignment, your sloppy project structure is _**other people's**_ problem. This creates a professional liability for you, because in addition to wasting other people's time, it makes you appear non-professional.

This is unnecessary and easy enough to fix before it happens.

## The folder within a folder problem that happens to new git users

There is a _**very common situation**_ that happens to new git users. The cause of this will not be discussed here, just the result.

Here is what the directory tree looks like when this typically happens

```
└── Assignment1
    └── Assignment1
        ├── css
        │   └── style.css
        ├── images
        │   └── screenshot.png
        └── my.html
```

Please notice there are two Assignment1 folders. The inner folder is where the work is, the outer folder is the code repository.

This feels like it works fine for the not-yet-professional student because he/she has VSCode and or Eclipse or ... opened to the inner folder. But then he/she pushes it up, shares the repository, and asks for assistance. This is where the problems start.

## What the professional assisting the student sees:

The professional who has been asked to assist the student attempts to open the project up and is confused and slowed down.

If it's a java project being imported into Eclipse, it is quadruply confusing because Eclipse doesn't even know how to import a folder within a folder where the inner folder has the Eclipse metadata files.

The assisting professional has to do a lot of extra work just to figure out what the problem is. By this time the not-yet-professional student has all but destroyed his/her professinal reputation, at least for the moment. And all because he/she did not have his/her project/repository set up properly.

## Here is how to fix it.

First, here is what the directory tree might looks like when this typically happens (copied from above)

```
└── Assignment1 (this is your repository folder)
    └── Assignment1 (this is your project folder)
        ├── css
        │   └── style.css
        ├── images
        │   └── screenshot.png
        └── my.html
```

Now, here is what it might look like after you fix it

```
└── Assignment1 (your repository folder and project folder are one and the same)
    ├── css
    │   └── style.css
    ├── images
    │   └── screenshot.png
    └── my.html
```

Please note that

0. Backing up your folder before you fix this (make a copy somewhere else) is a good idea if you are a rookie.
0. If Eclipse is involved, you may have to un-import first, then re-import after all this is done. 
1. When done, all project files are in the same configuration relative to each other
2. There is no inner folder and outer folder any more.
3. The files that were in the inner folder were moved to the outer folder.
4. What was the inner folder first became empty, then was deleted.
5. The repository folder and the project folder are now one and the same.

If this is confusing to you, get unconfused first!

Don't go and "fix it" thinking that you understand, then cry to someone for help because you acted before you thought things through, made a mess, and can't fix it any more.

You are a professional. These are the types of problems that professionals are expected to solve completely on their own. Think of this as a self-test, and don't accept a failure.

## Here is a step-by-step How-To guide to fix nested folders:

To help fix the nested folder issue, here are step-by-step instructions you can follow to restructure your project repository and eliminate the unnecessary folder within a folder setup:

### How to Fix Nested Folders (Folder within Folder Problem)

#### 1. **Back Up Your Project** 
   - Before making any changes, **back up** your project by copying the entire repository folder to a different location. This ensures you can recover your work if anything goes wrong.

#### 2. **Identify the Nested Folders**
   - In your project, you likely have a structure like this:
     ```
     └── Assignment1 (outer folder - repository)
         └── Assignment1 (inner folder - project)
             ├── css
             │   └── style.css
             ├── images
             │   └── screenshot.png
             └── my.html
     ```

#### 3. **Move Files from the Inner Folder to the Outer Folder**
   - Open your repository folder in **File Explorer (Windows)** or **Finder (macOS)**.
   - Navigate to the **inner folder** (`Assignment1` inside the outer `Assignment1`).
   - Select all the files and folders from inside the inner folder (such as `css`, `images`, `my.html`), and **move** them up one level to the **outer folder**.

#### 4. **Delete the Now-Empty Inner Folder**
   - Once you’ve moved all files, the inner folder (`Assignment1` within `Assignment1`) will be empty.
   - **Delete** the inner folder to ensure it no longer exists in your project structure.

#### 5. **Ensure Folder Structure is Correct**
   - After moving the files, your folder structure should now look like this:
     ```
     └── Assignment1 (repository folder)
         ├── css
         │   └── style.css
         ├── images
         │   └── screenshot.png
         └── my.html
     ```
   - This means your **repository folder and project folder are the same**.

#### 6. **Commit and Push Changes in GitHub Desktop**
   - Open **GitHub Desktop** and navigate to your project repository.
   - You will see the changes under the **Changes** tab (moving the files and deleting the inner folder).
   - Enter a **commit message** (e.g., "Restructure project by removing nested folders").
   - Click **Commit to master** (or the branch you’re working on).
   - **Push** the changes to your remote repository by clicking **Push origin**.

#### 7. **Re-import the Project into IDE (if necessary)**
   - If you're using **Eclipse**, **VS Code**, or any other IDE, you may need to:
     - **Un-import** the project from the IDE.
     - Then **re-import** the project after you have fixed the folder structure.
   - This ensures your IDE recognizes the updated project structure without confusion from the nested folders.

### Additional Tips:
- **Avoid creating a new nested folder when cloning a repository**: When cloning a repo, always specify the folder path where the repository should be placed, to avoid accidentally creating a nested directory.
