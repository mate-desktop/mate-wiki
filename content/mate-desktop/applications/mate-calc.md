---
title: MATE Calculator
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/mate-calc.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/mate-calc)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/mate-calc)](https://github.com/mate-desktop/mate-calc/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/mate-calc)](https://github.com/mate-desktop/mate-calc/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/mate-calc) | [Bug Tracker](https://github.com/mate-desktop/mate-calc/issues) | [Dependencies](https://github.com/mate-desktop/mate-calc/blob/master/.build.yml) | [Help](</mate-desktop/_includes/help/mate-calc-html/index.html>)



![](https://raw.githubusercontent.com/mate-desktop/mate-icon-theme/master/mate/48x48/apps/accessories-calculator.png)

{{< columns >}}

mate-calc  is the official calculator for the MATE Desktop Environment. It has been designed to be used with either the mouse or the keyboard. It is visually similar to a lot of hand-held calculators.

    <--->

[![](/mate-desktop/applications/images/mate-calc-window.png)](/mate-desktop/applications/images/mate-calc-window.png)

{{< /columns >}}

{{< expand "More">}}

SYNOPSIS

       mate-calc [OPTIONS...] [FILES...]

OPTIONS

       -s, --solve <equation>
              Solve the equation provided following this option.

       --version
              Output version information and exit.

       -h, -?, --help
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

