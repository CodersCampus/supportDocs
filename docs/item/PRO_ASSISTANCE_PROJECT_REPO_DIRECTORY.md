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

This works fine for the not-yet-professional student because he/she has VSCode opened to the inner folder. But then he/she pushes it up, shares the repository, and asks for assistance. This is where the problems start.

## What the professional assisting the student sees:

The professional who has been asked to assist the student attempts to open the project up and is confused and slowed down.

If it's a java project being imported into Eclipse, it is quadruply confusing because Eclipse doesn't even know how to import a folder within a folder where the inner folder has the Eclipse metadata files.

The assisting professional has to do a lot of extra work just to figure out what the problem is. By this time, the not-yet-professional student has all but destroyed his/her professinal reputation, at least for the moment. And all because he/she did not have his/her repository set up properly.