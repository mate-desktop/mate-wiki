---
title: Engrampa - File Archiver
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/engrampa.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/engrampa)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/engrampa)](https://github.com/mate-desktop/engrampa/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/engrampa)](https://github.com/mate-desktop/engrampa/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/engrampa) | [Bug Tracker](https://github.com/mate-desktop/engrampa/issues) | [Dependencies](https://github.com/mate-desktop/engrampa/blob/master/.build.yml)

![](https://raw.githubusercontent.com/mate-desktop/engrampa/master/data/icons/scalable/apps/engrampa.svg)

{{< columns >}}

Engrampa  is  the  official  archive  manager for the MATE Desktop Environment, it is a
graphical front-end to archiving utilities such as tar and zip. It is a  fork  of  File
Roller.

Engrampa  supports  most  common  operations such as creating, modifying and extracting
files from an archive. You can also view the contents of an archive and open files contained within the archive.

    <--->

[![](/mate-desktop/applications/images/engrampa-window.png)](/mate-desktop/applications/images/engrampa-window.png)

{{< /columns >}}


{{< expand "More">}}

SYNOPSIS

       engrampa [OPTIONS...] [FILES...]

OPTIONS

       filename(s)...
              Specifies  the  archive file to open when engrampa starts. If this is not speci‐
              fied, engrampa will start with a blank window and you may open an  archive  from
              the menu or by using the shortcut CTRL+O.

       -a, --add-to=ARCHIVE
              Add files to the specified archive and quit the program

       -d, --add FILE
              Add files asking the name of the archive and quit the program

       -e, --extract-to=FOLDER
              Extract archives to the specified folder and quit the program

       -f, --extract
              Extract archives asking the destination folder and quit the program

       -h, --extract-here
              Extract  archives using the archive name as destination folder and quit the pro‐
              gram

       --default-dir=FOLDER
              Default folder to use for the '--add' and '--extract' commands

       --force
              Create destination folder without asking confirmation

       --display=DISPLAY
              X display to use.

       -?, --help
              Print standard command line options.

       --help-all
              Print all command line options.

       --version
              Show the application's version.

       This program also accepts the standard GTK options.

{{< /expand >}}

## Build / Install

Simple build procedure:

```
$ git submodule update --init --recursive   # Init Git submodules
$ ./autogen.sh --prefix=/usr                # Build configuration
$ make                                      # Build
```
For installation to a separate prefix change the above `./autogen.sh` command to:

```
$ ./autogen.sh --prefix=/an/other/path
```

After building the package you may install it:

```
[ Become root if necessary ]
$ make install                              # Installation
```

