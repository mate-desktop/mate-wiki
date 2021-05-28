---
title: Mozo - Menu Editor
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/mozo.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/mozo)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/mozo)](https://github.com/mate-desktop/mozo/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/mozo)](https://github.com/mate-desktop/mozo/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/mozo) | [Bug Tracker](https://github.com/mate-desktop/mozo/issues) | [Dependencies](https://github.com/mate-desktop/mozo/blob/master/.build.yml)

![](https://raw.githubusercontent.com/mate-desktop/mozo/master/data/icons/hicolor_apps_48x48_mozo.png)

{{< columns >}}

Mozo is a menu editor for MATE using the freedesktop.org menu specification. It is a
fork of Alacarte.

    <--->

[![](/mate-desktop/applications/images/mozo-window.png)](/mate-desktop/applications/images/mozo-window.png)

{{< /columns >}}

{{< expand "More">}}

SYNOPSIS

       mozo

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

