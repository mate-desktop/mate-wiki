---
title: marco - Window Manager
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/marco.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/marco)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/marco)](https://github.com/mate-desktop/marco/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/marco)](https://github.com/mate-desktop/marco/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/marco) | [Bug Tracker](https://github.com/mate-desktop/marco/issues) | [Dependencies](https://github.com/mate-desktop/marco/blob/master/.build.yml)

![](https://raw.githubusercontent.com/mate-desktop/mate-icon-theme/master/mate/48x48/apps/preferences-system-windows.png)

Marco  is  a minimal X window manager that uses GTK+ for drawing window
frames. It is aimed at non-technical users and is designed to integrate
well  with  the  MATE  desktop. Marco is a plain window manager for the
adult in you; Many window managers are like  Marshmallow  Froot  Loops,
Marco  is like Cheerios. It lacks some features that may be expected by
traditional UNIX or other technical users; these users may want to  investigate  other  available window  managers for use with MATE or as a standalone window manager.

Marco supports several somewhat advanced but common  features  such  as
Window  Shading/Roll-Up,  Window/Edge Snapping, Vertical and Horizontal
Maximize, Always-On-Top,  Sloppy/Mouse  Focus  and  Raising,  and  many
more... Well, not a lot, but some more.

{{< expand "More">}}

SYNOPSIS

       marco [OPTIONS]

OPTIONS

       -d, --display=DISPLAY
              X display to use.

       --sync
              Make X calls synchronous.

       --replace
              Replace the currently running window manager with Marco.

       --sm-disable
              Disable the connection to the session manager.

       --sm-client-id=ID
              Specify a session management ID.

       --sm-save-file=FILENAME
              Restore from a session management savefile.
              If  no  path is specified marco will look in ~/.config/mate-ses‐
              sion/saved-session/

       -c, --composite
              Turn compositing ON. You may also use this option to start marco
              with composite "true transparency" effects.

       --no-composite
              Turn  compositing  OFF.  You  may  also use this option to start
              marco without compositing effects.

       --no-force-fullscreen
              Do not create fullscreen windows without decorations.

       --version
              Print current version information and exit.

       -?, -h, --help
              Print standard command line options.

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


