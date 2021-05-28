---
title: EoM - Image Viewer
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/eom.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/eom)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/eom)](https://github.com/mate-desktop/eom/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/eom)](https://github.com/mate-desktop/eom/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/eom) | [Bug Tracker](https://github.com/mate-desktop/eom/issues) | [Dependencies](https://github.com/mate-desktop/eom/blob/master/.build.yml) | [API Documentation](/mate-desktop/_includes/api-doc/eom-html/index.html)

![](https://raw.githubusercontent.com/mate-desktop/eom/master/data/icons/scalable/apps/eom.svg)

{{< columns >}}

eom or the Eye of MATE is the official image viewer for the MATE  Desktop  Environment. It  aims  to be simplistic, lightweight, and easy to use. The Eye of MATE may also be used to perform basic tasks like image flipping and rotation.

Eye  of MATE features a flexible plugin system which can be used to dynamically add new advanced features to eom itself. eom  uses  the  gdk-pixbuf  library,  it can handle large images, zoom, and scroll with low memory usage.

    <--->

[![](/mate-desktop/applications/images/eom-window.png)](/mate-desktop/applications/images/eom-window.png)

{{< /columns >}}

{{< expand "More">}}

SYNOPSIS

       eom  [--fullscreen]  [--disable-image-collection] [--slide-show] [--new
       instance] [FILES...]


OPTIONS

       filename(s)...
              Specifies the image to open when eom  starts.  If  this  is  not
              specified, eom will start with a blank window and you may open a
              file from the menu or by using the  shortcut  CTRL+O.  eom  also
              supports handling of remote files.

       --display=DISPLAY
              X display to use.

       -f, --fullscreen
              Start eom in fullscreen mode.

       -c, --disable-image-collection
              Disable image collection viewer.

       -s, --slide-show
              Open in slideshow mode.

       -n, --new-instance
              Start a new instance instead of reusing an existing window.

       --version
              Output version information and exit.

       -h, --help
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

