---
title: Building and Installing
weight: -10
---

To run the newest version of a MATE project, often it is not enough to build it from source (i.e. it can not be executed with `./my-program`). To work properly it need to be installed, because the installation process ensures that all the needed files are copied to the right places.

{{< toc >}}


## Building

First make sure you have all dependencies of the package installed:

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

All MATE applications are built in the same way:

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

## Uninstall

To uninstall just do:

```
[ Become root if necessary ]
$ make uninstall
```

