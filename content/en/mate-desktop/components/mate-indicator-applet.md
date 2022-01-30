---
title: mate-indicator-applet
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/mate-indicator-applet.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/mate-indicator-applet)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/mate-indicator-applet)](https://github.com/mate-desktop/mate-indicator-applet/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/mate-indicator-applet)](https://github.com/mate-desktop/mate-indicator-applet/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/mate-indicator-applet) | [Bug Tracker](https://github.com/mate-desktop/mate-indicator-applet/issues) | [Dependencies](https://github.com/mate-desktop/mate-indicator-applet/blob/master/.build.yml)

![](https://raw.githubusercontent.com/mate-desktop/mate-icon-theme/master/mate/48x48/actions/system-run.png)

mate-indicator-applet is a small applet to display information from various applications consistently in the panel. The indicator applet exposes Ayatana Indicators in the MATE Panel. Ayatana Indicators are an initiative by Canonical to provide crisp and clean system and application status indication. They take the form of an icon and associated menu, displayed (usually) in the desktop panel. Existing indicators include the Message Menu, Battery Menu and Sound menu.

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


