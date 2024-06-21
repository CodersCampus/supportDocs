# Structuring Your Project Repository

Theoretically, if your project is strictly private, then it is your own business what you do inside it.

This does not apply, if you are asking others for assistance.

## The folder within a folder problem that happens to new git users

There is a very common situation that happens to new git users. The cause of this will not be discussed here, just the result.

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

The assisting professional has to do a lot of extra work just to figure out what the problem is. By this time, the not-yet-professional student has all but destroyed his/her professinal reputation, at least for the moment. And all because he/she did not have his/her repository set up properly.

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

0. Backing up your folder (make a copy somewhere else) is a good idea if you are a rookie.
0. If Eclipse is involved, you may have un-import first, then re-import after all this is done. 
1. When done, all project files are in same configuration relative to each other
2. There is no inner folder and outer folder any more
3. The files that were in the inner folder were moved to the outer folder
4. What was the inner folder first became empty, then was deleted
5. The repository folder and the project folder are now one and the same

If this is confusing to you, get unconfused first!

Don't go and "fix it" thinking that you understand, then cry to someone for help because you acted before you thought things through, made a mess, and can't fix it any more.

You are a professional. These are the types of problems that professionals are expected to solve completely on their own. Think of this as a self-test, and don't accept a failure.