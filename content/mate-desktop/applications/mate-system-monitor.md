---
title: MATE System Monitor
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/mate-system-monitor.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/mate-system-monitor)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/mate-system-monitor)](https://github.com/mate-desktop/mate-system-monitor/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/mate-system-monitor)](https://github.com/mate-desktop/mate-system-monitor/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/mate-system-monitor) | [Bug Tracker](https://github.com/mate-desktop/mate-system-monitor/issues) | [Dependencies](https://github.com/mate-desktop/mate-system-monitor/blob/master/.build.yml)

![](https://raw.githubusercontent.com/mate-desktop/mate-icon-theme/master/mate/48x48/apps/utilities-system-monitor.png)

{{< columns >}}

The  mate-system-monitor  allows  you to view and control the processes running on your
system. You can access detailed memory maps, send signals, and terminate the processes.

In addition, the mate-system-monitor provides an overall view of the resource usage  on
your system, including memory and CPU allocation, as well as network usage. It also allows you to view file system information such as Device, Type,  Mountpoints,  and  Disk Usage.

The  System tab will display basic information about your system like Hostname, Kernel, MATE Version, Installed Memory, and Processor Information.

    <--->

[![](/mate-desktop/applications/images/mate-system-monitor-window.png)](/mate-desktop/applications/images/mate-system-monitor-window.png)

{{< /columns >}}


{{< expand "More">}}

SYNOPSIS

       mate-system-monitor [OPTIONS]

OPTIONS

       This program accepts all the standard MATE and GTK+ options, which follow the usual GNU
       command  line syntax, with long options starting with two dashes ('-').  In addition to
       those standard MATE options, the mate-system-monitor accepts the following options:

       -s, --show-system-tab
              Show the System tab.

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

