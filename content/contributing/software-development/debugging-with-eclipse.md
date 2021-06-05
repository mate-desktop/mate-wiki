---
title: Debugging with Eclipse
weight: -10
---

This page details the generic process for debugging the MATE desktop environment with Eclipse IDE.

{{< toc >}}

## Setting up the development environment

The installation of the development environment can be done anywhere, on this page we will install it on user home folder.

The installation process involves downloading the *Eclipse IDE for C/C++ Developers* package from https://www.eclipse.org/downloads/packages/, installing the IDE in the ~/eclipse folder, and running the script to install the debugging plugin in the ~/cdtdebugger folder.

Before you begin this procedure, make sure you have a java runtime environment installed on your system.

1. Download *Eclipse IDE for C/C++ Developers* package from https://www.eclipse.org/downloads/packages/ on your home folder.
2. Extract the tarball on your home folder. After performing this step the IDE will be installed in the folder ~/eclipse:
```
$ tar xzvf eclipse-cpp-2019-12-R-linux-gtk-x86_64.tar.gz
```
3. Install the debugger plugin on your home folder. After performing this step the debugger plugin will be installed in the folder ~/cdtdebugger:
```
$ chmod +x ./eclipse/plugins/org.eclipse.cdt.debug.application_1.1.400.201910171407/scripts/install.sh
$ ./eclipse/plugins/org.eclipse.cdt.debug.application_1.1.400.201910171407/scripts/install.sh
```

To start the debugger, just run the command below:

```
$ ~/cdtdebugger/cdtdebug.sh
```

## Enabling the debug of a MATE component

The generic way to enable debug is to set the debugging flag and disable optimizations on the configuration process, which is performed before the make.

In the example below we want to install Caja with debugging enabled, for doing this we will first have to download a copy of the source code, then we will have to configure it with debugging enabled and finally we will install it on the system.

1. Download the source code of Caja:
```
$ git clone https://github.com/mate-desktop/caja.git
```
2. Configure with debugging enabled (-g) and without optimizations (-O0):
```
$ CFLAGS="-g -O0" ./autogen.sh --prefix=/usr
```
3. Build
```
$ make
```
4. Install
```
$ sudo make install
```
TIP: Before performing the second step, all build dependencies must be installed, you can use your favorite package manager to do so. On Fedora you can run:
```
$ sudo dnf builddep caja
```

## Debugging a MATE component

This is without a doubt the key point as it may vary depending on the component you want to debug. There are two possible cases. Debug an application that is running or debug an application by launching it.

### To debug an application that is running
Run the command below:
```
$ ~/cdtdebugger/cdtdebug.sh -a PID
```
Example:
```
$ ~/cdtdebugger/cdtdebug.sh -a $(pgrep caja)
```
Or you can also run the `~/cdtdebugger/cdtdebug.sh` without any arguments, close *Debug New Executable* dialog, select File -> Debug Attached Executable from main menu and select the process on next dialog.

You will need to terminate any running process before debugging a newly installed binary.

If you want **to debug a library**, just debug the component that uses it and add the library on the executables list. Let's say we want to debug the Caja plugin "image-converter", and we installed and enabled the debugging of:

- https://github.com/mate-desktop/caja.git
- https://github.com/mate-desktop/caja-extensions.git

First we start the debugging of the Caja process:
```
$ ~/cdtdebugger/cdtdebug.sh -a $(pgrep caja)
```
Then we import the file /usr/lib64/caja/extensions-2.0/libcaja-image-converter.so into the executable tab.

To add a breakpoint just click on libcaja-image-converter.so in the *Executables* tab, double click on a *Source File Name* row to show the content of file, and press Shift+Control+B to toggle a breakpoint on the desired line.

TIP: You can debug marco through a remote connection:
```
$ ssh -Y user@host
$ ~/cdtdebugger/cdtdebug.sh -a $(pgrep marco)
```

### To debug an application by launching it
Run the command below:
```
$ ~/cdtdebugger/cdtdebug.sh -e EXEC ARGS
```
Example:
```
$ ~/cdtdebugger/cdtdebug.sh -e /usr/bin/engrampa --add-to=backup.tar.gz ~/caja
```
In the example above, **engrampa** was installed with debugging enabled:

- https://github.com/mate-desktop/engrampa.git

To add a breakpoint just click on engrampa in the *Executables* tab, double click on a *Source File Name* row to show the content of file, and press Shift+Control+B to toggle a breakpoint on the desired line.

If the executable does not appear in the list you can **import** it.
