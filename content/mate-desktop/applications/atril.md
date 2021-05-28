---
title: Atril - PDF Viewer
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/atril.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/atril)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/atril)](https://github.com/mate-desktop/atril/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/atril)](https://github.com/mate-desktop/atril/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/atril) | [Bug Tracker](https://github.com/mate-desktop/atril/issues) | [Dependencies](https://github.com/mate-desktop/atril/blob/master/.build.yml)

![](https://raw.githubusercontent.com/mate-desktop/atril/master/data/icons/scalable/apps/atril.svg)

{{< columns >}}
Atril  is the official Document Viewer of the MATE Desktop Environment,
it is a simple multi-page document viewer. It  can  display  and  print
PostScript (PS), Encapsulated PostScript (EPS), DJVU, DVI, XPS and Portable Document Format (PDF) files.

When supported by the document, it  also  allows  searching  for  text,
copying  text to the clipboard, hypertext navigation, and table-of-contents bookmarks.

    <--->

[![](/mate-desktop/applications/images/atril-window.png)](/mate-desktop/applications/images/atril-window.png)

{{< /columns >}}



{{< expand "More">}}

SYNTAX

       atril [OPTIONS...] [FILES...]

OPTIONS

       filename(s)...
              Specifies the file to open when atril starts.  If  this  is  not
              specified, atril will start with a blank window and you may open
              a file from the menu or by using the shortcut  CTRL+O.  Multiple
              files  can be loaded if they are separated by spaces. atril also
              supports handling of remote files.

       -p, --page-label=PAGE
              Here you can specify a page label, this page will be selected in
              the document if it exists.

       -i, --page-index=NUMBER
              Here  you  can specify a page number, this page will be selected
              in the document if it exists.

       -f, --fullscreen
              Start atril in fullscreen mode. You must specify a  document  to
              start in fullscreen mode.

       -s, --presentation
              Start atril in presentation mode. You must specify a document to
              start in presentation mode.

       -w, --preview
              Start atril in preview mode. You  must  specify  a  document  to
              start in preview mode.

       --display=DISPLAY
              X display to use.

       --version
              Output version information and exit.

       -?, -h, --help
              Print standard command line options.

       --help-all
              Print all command line options.

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

