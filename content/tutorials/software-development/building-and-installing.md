---
title: Building and Installing
weight: -10
---

Often it is not enough to build the MATE applications from source. To work properly they need to be installed (i.e. they can not be executed with `./my-program`), because the installation process ensures that all the needed files are copied to the right places.

{{< toc >}}


## Building

First make sure you have all dependencies installed:

{{< tabs >}}
{{< tab "Debian/Ubuntu/Linux Mint" >}}

```
$ sudo apt build-dep <package-name>
```
{{< /tab >}}
{{< tab "Fedora" >}}
```
$ sudo dnf builddep <package-name>
```
{{< /tab >}}
{{< /tabs >}}

All MATE applications are built in the same way.

Simple build procedure:

```
$ git submodule update --init --recursive   # Init Git submodules
$ ./autogen.sh --prefix=/usr                # Build configuration
$ make                                      # Build
```

## Installing

Warning: This procedure doesn't install in a separate prefix, so it may overwrite your system binaries.

After building the package you may install it:

```
[ Become root if necessary ]
$ make install                              # Installation
```

