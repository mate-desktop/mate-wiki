---
title: First Contribution
weight: -15
---

If you are looking to make your first contribution, follow the steps below.

{{< toc >}}

## Fork the repository

Fork the repository by clicking on the fork button on the top of the Github page of the MATE package.
This will create a copy of this repository in your account.

## Clone the repository

Now clone the forked repository to your machine. Go to your GitHub account, open the forked repository, click on the code button and then click the _copy to clipboard_ icon.

Open a terminal and run the following git command:

```
git clone url-you-just-copied
```

where `url-you-just-copied` is the url to this repository (your fork of this project).

For example:

```
git clone https://github.com/this-is-you/mate-calc
```

where `this-is-you` is your GitHub username. Here you're copying the contents of the repository on GitHub to your computer.

## Create a branch

Change to the repository directory on your computer (if you are not already there).

Now create a branch using the `git checkout` command:

```
git checkout -b your-new-branch-name
```

For example:

```
git checkout -b better-factorization
```

## Make some changes and commit those changes

Now open the source code files that you would like to change in a text editor.

Make some changes. To test if your changes are working correctly you probably need to build and install the project.

If you go to the project directory and execute the command `git status`, you'll see there are changes.

Add those changes to the branch you just created using the `git add` command:

```
git add modified-file.c
```

Replace `modified-file.c` with the name of the file you actually edited.

Now commit those changes using the `git commit` command:

```
git commit -m "Commit Message"
```

replacing `Commit Message` with something meaningful that describes your changes.

## Push changes to GitHub

Push your changes using the command `git push`:

```
git push origin add-your-branch-name
```

replacing `add-your-branch-name` with the name of the branch you created earlier.

## Submit your changes for review

If you go to your repository on GitHub, you'll see a `Compare & pull request` button. Click on that button.

Now submit the pull request.


