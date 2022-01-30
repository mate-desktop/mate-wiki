---
title: mate-panel
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/mate-panel.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/mate-panel)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/mate-panel)](https://github.com/mate-desktop/mate-panel/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/mate-panel)](https://github.com/mate-desktop/mate-panel/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/mate-panel) | [Bug Tracker](https://github.com/mate-desktop/mate-panel/issues) | [Dependencies](https://github.com/mate-desktop/mate-panel/blob/master/.build.yml)

![](https://raw.githubusercontent.com/mate-desktop/mate-panel/master/icons/48x48/mate-panel.png)

The  mate-panel program provides the panels for the the MATE Desktop Environment. It is
the area on your desktop from which you can run applications and applets,  and  perform
other tasks. New applets may also be installed ,added to, or removed from the panels.

By  default, mate-panel typically creates a panel on the top of the screen with applets
such as a Menu Bar, Notification Area, and Clock; While creating a second panel on  the
bottom  of  the  screen with a Window List and a Workspace Switcher. Panels can be created, deleted, moved around the desktop, and to other monitors.

{{< expand "More">}}

SYNOPSIS

       mate-panel [OPTIONS]

OPTIONS

       --replace
              Replace a currently running instance of mate-panel.

       --reset
              Reset the panel configuration to the default setting.

       --run-dialog
              Open the "Run Application" dialog, also accessible by pressing ALT+F2.

       --display=DISPLAY
              X display to use.

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

