---
title: Getting Started
weight: -20
---

We assume you to have basic coding knowledge. If you don't, we recommend that you read the chapters *Introduction*, *Beginning C* and *Intermediate C* of the [C Wikibook](https://en.wikibooks.org/wiki/C_Programming) and make some exercises (or something equivalent).

The MATE Desktop is mostly written in C. Some projects are written in Python or C++.

You should already have a text editor like [Pluma](/mate-desktop/applications/pluma), Gedit or Kate and a terminal application like [MATE Terminal](/mate-desktop/applications/mate-terminal) installed. Alternatively you could use a fully featured IDE such as [VSCodium](https://vscodium.com/), [Eclipse](https://www.eclipse.org/) or [Code::Blocks](https://www.codeblocks.org/).

If you never developed a big application in a team before, your basic workflow was probably like this: You edited some source (.c, .cpp, .py) files and maybe some header files (.h, .hpp), compiled them (probably using `gcc my-program` or hitting the *compile* button in your IDE) and finally executed your program (with `./my-program` or `python3 my-program` or hitting the *run* button on your IDE).

In the following we shortly explain some tools, that are generally used by larger software projects (i.e. by the MATE Desktop) that ease the developing process.

{{< toc >}}

## Makefiles

MATE packages usually are a lot bigger than just a handful of source files. In addition to (usually >30) source files, they include language files, settings files, desktop files, help files and so on. Compiling a MATE application with the above approach would be very tedious: All source files would be recompiled even if you only edited one. Also, if you lose the compile command or switch computers you have to retype it from scratch. This is why Makefiles were introduced. A Makefile is basically a text file, which consists of rules which tell the compiler how to do its job.

{{< hint ok >}}

Makefile Tutorial: https://cs.colby.edu/maxwell/courses/tutorials/maketutor/

{{< /hint >}}

## Git

[Git](https://git-scm.com/) is software for tracking changes in any set of files, usually used for coordinating work among programmers collaboratively developing source code during software development. Its goals include speed, data integrity, and support for distributed, non-linear workflows (thousands of parallel branches running on different systems).

{{< hint ok >}}

gittutorial - A tutorial introduction to Git: https://git-scm.com/docs/gittutorial

giteveryday - A useful minimum set of commands for Everyday Git: https://git-scm.com/docs/giteveryday

Git Cheat Sheet: https://training.github.com/downloads/github-git-cheat-sheet/

{{< /hint >}}

## Github

[Github](https://github.com/) is the place where we host our Git repositories. If you want to contribute to the MATE Desktop Environment you will need to create a free account at Github.

{{< hint ok >}}

Github Docs - Collaborating with pull requests: https://docs.github.com/en/github/collaborating-with-pull-requests

{{< /hint >}}

## Virtualisation

If you need to rely on a stable system you can do MATE development in a safe environment, for example by using virtualisation. You can use a virtualisation application such as [GNOME Boxes](https://help.gnome.org/users/gnome-boxes/stable/) or [VirtualBox](https://virtualbox.org) and setup a virtual machine by [installing](/introduction/installation/#preinstalled) a distribution specifically for developing MATE applications.

{{< hint ok >}}

Help for GNOME Boxes: https://help.gnome.org/users/gnome-boxes/stable/

User Manual for VirtualBox: https://www.virtualbox.org/manual/UserManual.html#intro-running

{{< /hint >}}

