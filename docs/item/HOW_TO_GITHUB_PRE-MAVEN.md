# Setting Up a Git Repository and Pushing Code (Until You Learn Maven)

## Step 1: Create a Git Repository in Eclipse

1. In Eclipse, click `File` > `New` > `Other`.
2. Locate the `Git` folder and click `Git Repository`.
3. Do not create a bare repository, and click `Finish`.
4. Open the Git perspective by going to `Window` > `Perspective` > `Open Perspective` > `Other` > `Git`.
5. You should now see your repository in the Explorer.

## Step 2: Create a Java Project

1. Go back to the Java view by clicking `File` > `New` > `Java Project`.
2. Deselect `Use Default Folder`, click `Browse`, and navigate to the `user/directory/git/folder/new assignment` folder.
3. Click `Next`, check `JDK 11` (or go to `Edit Library` and select `JDK 11` there), and then click `Finish`.

## Step 3: Add Code to GitHub Desktop

1. After creating some code/classes in your assignment, open GitHub Desktop.
2. Click `File` > `Add local repo`, navigate to the new repository directory location, and then deselect `.classpath`, `.project`, and `.class` (these are Eclipse files that don't need to be committed to the remote GitHub repository).

## Step 4: Configure Ignored Files

1. In GitHub Desktop, click `Repository` > `Repo settings` > `Ignored Files`.
2. Add `/bin/`, `.classpath`, `.project` (and `.DS_Store` for Mac users), then save. You should now see the `.gitignore` file with these ignored file types.

## Step 5: Publish the Repository

1. Add a summary and deselect `Keep this code private`.
2. Click `Publish Repository`.
3. Add a commit message and commit, then click `Push`.

## Step 6: Verify the Repository on GitHub

1. Go to your GitHub.com profile and click on `Repositories` (or refresh the page).
2. You should now see the new repository.

## Step 7: Commit and Push Changes

Anytime you add new code, commit and push the changes. You can do this multiple times a day, as needed.

Remember, this is a temporary workflow until you learn how to use Maven. Following these steps will help you set up a Git repository, connect it to your local development environment, and push your code changes to the remote repository on GitHub.