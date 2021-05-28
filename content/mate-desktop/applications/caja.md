---
title: Caja - File Manager
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/caja.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/caja)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/caja)](https://github.com/mate-desktop/caja/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/caja)](https://github.com/mate-desktop/caja/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/caja) | [Bug Tracker](https://github.com/mate-desktop/caja/issues) | [Dependencies](https://github.com/mate-desktop/caja/blob/master/.build.yml)

![](https://raw.githubusercontent.com/mate-desktop/mate-icon-theme/master/mate/48x48/apps/system-file-manager.png)

{{< columns >}}

Caja  is the default file manager for the MATE Desktop Environment. It makes it easy to
manage, manipulate, and customize files and directories. Caja can access local and  remote filesystems such as SSH, FTP, and WebDav (HTTP/HTTPS).

Caja also provides the desktop background and the icons it uses for launching links and
applications, as well as accessing files, directories, the trash, and  removable  media
like CD/DVD/BD and USB drives.

    <--->

[![](/mate-desktop/applications/images/caja-window.png)](/mate-desktop/applications/images/caja-window.png)

{{< /columns >}}


{{< expand "More">}}

SYNOPSIS

       caja [OPTIONS...] [URI...]

OPTIONS

       --browser
              Open a browser window.

       -c, --check
              Perform a quick set of self-check tests.

       --display=DISPLAY
              X display to use.

       -g, --geometry=GEOMETRY
              Create the initial window with the given geometry.

       -t, --tabs
              Open URIs in tabs.

       -n, --no-default-window
              Only create windows for explicitly specified URIs.

       --no-desktop
              Do not manage the desktop (ignore the preference set in the preferences dialog).

       --force-desktop
              Manage  the desktop regardless of set preferences or environment (on new startup
              only)

       -q, --quit
              Quit Caja.

       --version
              Print current version information and exit.

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

