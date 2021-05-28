---
title: MATE Terminal
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/mate-terminal.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/mate-terminal)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/mate-terminal)](https://github.com/mate-desktop/mate-terminal/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/mate-terminal)](https://github.com/mate-desktop/mate-terminal/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/mate-terminal) | [Bug Tracker](https://github.com/mate-desktop/mate-terminal/issues) | [Dependencies](https://github.com/mate-desktop/mate-terminal/blob/master/.build.yml)

![](https://raw.githubusercontent.com/mate-desktop/mate-icon-theme/master/mate/48x48/apps/utilities-terminal.png)

{{< columns >}}

Mate Terminal is the official terminal emulator for the MATE Desktop.

    <--->

[![](/mate-desktop/applications/images/mate-terminal-window.png)](/mate-desktop/applications/images/mate-terminal-window.png)

{{< /columns >}}


{{< expand "More">}}

   Usage:

      mate-terminal [OPTION...]

   Help Options:

       -h, --help
              Show help options

       --help-all
              Show all help options

       --help-terminal
              Show terminal options

       --help-window-options
              Show per-window options

       --help-terminal-options
              Show per-terminal options

       --help-gtk
              Show GTK+ Options

       --help-sm-client
              Show session management options

   Options to open new windows or terminal tabs; more than one of these may be specified:

       --window
              Open a new window containing a tab with the default profile

       --tab  Open a new tab in the last-opened window with the default profile

   Window  options;  if used before the first --window or --tab argument, sets the default for
       all windows:

       --show-menubar
              Turn on the menubar

       --hide-menubar
              Turn off the menubar

       --maximize
              Maximize the window

       --full-screen
              Full-screen the window

       --geometry=GEOMETRY
              Set the window size; for example: 80x24, or 80x24+200+200 (COLSxROWS+X+Y)

       --role=ROLE
              Set the window role

       --active
              Set the last specified tab as the active one in its window

   Terminal options; if used before the first --window or --tab argument, sets the default for
       all terminals:

       -e, --command
              Execute the argument to this option inside the terminal

       -x, --execute
              Execute the remainder of the command line inside the terminal

       --profile=PROFILE-NAME
              Use the given profile instead of the default profile

       -t, --title=TITLE
              Set the terminal title

       --working-directory=DIRNAME
              Set the working directory

       --zoom=ZOOM
              Set the terminal's zoom factor (1.0 = normal size)

       GTK+ Options

       --class=CLASS
              Program class as used by the window manager

       --name=NAME
              Program name as used by the window manager

       --screen=SCREEN
              X screen to use

       --sync Make X calls synchronous

       --gtk-module=MODULES
              Load additional GTK+ modules

       --g-fatal-warnings
              Make all warnings fatal

   Session management options:

       --sm-client-disable
              Disable connection to session manager

       --sm-client-state-file=FILE
              Specify file containing saved configuration

       --sm-client-id=ID
              Specify session management ID

   Application Options:

       --disable-factory
              Do not register with the activation nameserver, do not re-use an active terminal

{{< /expand >}}

## Build / Install

***Meson***

Simple build procedure:

```
$ meson build --prefix=/usr                 # Build configuration
$ cd build
$ ninja                                     # Build
```

After building the package you may install it:

```
[ Become root if necessary ]
$ ninja install                              # Installation
```

***Autotools***

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
