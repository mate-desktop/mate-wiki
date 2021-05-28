---
title: Pluma - Text Editor
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/pluma.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/pluma)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/pluma)](https://github.com/mate-desktop/pluma/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/pluma)](https://github.com/mate-desktop/pluma/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/pluma) | [Bug Tracker](https://github.com/mate-desktop/pluma/issues) | [Dependencies](https://github.com/mate-desktop/pluma/blob/master/.build.yml)

![](https://raw.githubusercontent.com/mate-desktop/mate-icon-theme/master/mate/48x48/apps/accessories-text-editor.png)

{{< columns >}}

Pluma is the official text editor of the MATE desktop environment. While aiming at simplicity and ease of use, Pluma is a powerful general purpose text  editor.  It  can  be used to create and edit all sorts of text files.

Pluma  features  a  flexible plugin system which can be used to dynamically add new advanced features to Pluma itself.

    <--->

[![](/mate-desktop/applications/images/pluma-window.png)](/mate-desktop/applications/images/pluma-window.png)

{{< /columns >}}

{{< expand "More">}}

SYNOPSIS

       pluma [OPTIONS...] [FILES...]

OPTIONS

       filename(s)...
              Specifies the file to open when pluma starts. If this is  not  specified,  pluma
              will  start  a  new, blank file with an "Unsaved Document" label. Multiple files
              can be loaded if they are separated by spaces. pluma also supports  handling  of
              remote files.

       --display=DISPLAY
              X display to use.

       --encoding
              Set  the  character encoding to be used for opening the files listed on the com‐
              mand line.

       --new-window
              Create a new toplevel window in an existing instance of pluma.

       --new-document
              Create a new document in an existing instance of pluma, on the last Pluma window
              that had focus.

       +[num] For the first file, go to the line specified by "num" (do not insert a space be‐
              tween the "+" sign and the number).  If "num" is missing, go to the last line.

       --list-encodings
              Display list of possible values for the encoding option and exit

       --version
              Output version information and exit

       -?, -h, --help
              Print standard command line options.

       --help-all
              Print all command line options.

       This program also accepts the standard GTK options.

{{< /expand >}}

## Build / Install

Simple build procedure:

```
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

