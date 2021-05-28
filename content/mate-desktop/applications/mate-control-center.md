---
title: MATE Control Center
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/mate-control-center.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/mate-control-center)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/mate-control-center)](https://github.com/mate-desktop/mate-control-center/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/mate-control-center)](https://github.com/mate-desktop/mate-control-center/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/mate-control-center) | [Bug Tracker](https://github.com/mate-desktop/mate-control-center/issues) | [Dependencies](https://github.com/mate-desktop/mate-control-center/blob/master/.build.yml)

![](https://raw.githubusercontent.com/mate-desktop/mate-icon-theme/master/mate/48x48/categories/preferences-desktop.png)

{{< columns >}}

mate-control-center is a graphical user interface to configure various aspects of MATE.

When run without arguments, the shell displays the control center overview, which shows
all available configuration panels. The overview allows one to open individual panels
by clicking on them. It also has a search entry to find panels by searching keywords.

    <--->

[![](/mate-desktop/applications/images/mate-control-center-window.png)](/mate-desktop/applications/images/mate-control-center-window.png)

{{< /columns >}}

{{< expand "More">}}

SYNOPSIS

       mate-control-center [OPTION...]

OPTIONS

       -?, --help
              Print the application's help options and exit.

       --help-gtk
              Print GTK help options and exit.

       --help-all
              Print application and GTK help options and exit.

       --hide Hide on start (useful for preloading the shell).

       --display=DISPLAY
              X display to use.

       This program additionally accepts the standard MATE and GTK options (as listed with
       --help-gtk)

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

