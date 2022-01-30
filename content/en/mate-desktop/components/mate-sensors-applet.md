---
title: mate-sensors-applet
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/mate-sensors-applet.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/mate-sensors-applet)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/mate-sensors-applet)](https://github.com/mate-desktop/mate-sensors-applet/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/mate-sensors-applet)](https://github.com/mate-desktop/mate-sensors-applet/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/mate-sensors-applet) | [Bug Tracker](https://github.com/mate-desktop/mate-sensors-applet/issues) | [Dependencies](https://github.com/mate-desktop/mate-sensors-applet/blob/master/.build.yml)

![](https://raw.githubusercontent.com/mate-desktop/mate-icon-theme/master/mate/48x48/actions/system-run.png)

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

