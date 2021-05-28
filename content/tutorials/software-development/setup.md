---
title: Setup a development environment
weight: -20
---

{{< toc >}}

## Initial Setup

A development environment is a set of tools which assist you in developing. For MATE Desktop development a simple text editor like [Pluma](/mate-desktop/applications/pluma), Gedit or Kate a terminal and git is enough. Of course you can use fully featured IDEs such as [VSCodium](https://vscodium.com/), [Eclipse](https://www.eclipse.org/) or [Code::Blocks](https://www.codeblocks.org/) as well.

[Git](https://git-scm.com/) is a free and open source distributed version control system. It helps people to develop a program together at the same time. If you do not know how to use git don't worry, it is [very simple to use](https://rogerdudler.github.io/git-guide/).

The distribution you are currently using is probably a good choice. For some MATE applications you will need recent versions of some libraries so make sure you use a reasonable recent version of your distribution. If you run Windows or MacOS you can still help developing MATE, see [Virtualisation](#virtualisation).

For most development and testing tasks you will need to install the latest version of the application in question. That is, clone it from the master branch, build it and install that newest version onto your system. If you do not want to alter the system you are currently running, there are two options.

### Virtualisation

You can use a virtualisation application such as [GNOME Boxes](https://help.gnome.org/users/gnome-boxes/stable/) or [VirtualBox](https://virtualbox.org). Setup a virtual machine by [installing](/introduction/installation) a Linux distribution of your choice.

{{< hint info >}}
A virtual machine is a simulated computer running inside another computer. The simulated computer is often called guest, while the real machine is called host.
With virtualisation, the guest has access to the real hardware the host is running. If the guest can run on fake hardware, it's called emulation. [source](https://help.gnome.org/users/gnome-boxes/stable/what-is-a-virtual-machine.html.en)
{{< /hint >}}

Now you can start developing inside that virtual machine without making changes to your current system.

### Dual Booting

You can also [install](/introduction/installation) a distribution that you use only for developing and testing the MATE Desktop [alongside](https://en.wikipedia.org/wiki/Multi-booting) the system you are currently running. That way you do not have to make any changes to your current system.

### Overwriting system binaries

The easiest but also the riskiest way is to use the Linux distribution of your choice and build and install the MATE application you like to help developing onto your system (possibly overwriting system binaries). Note that if you need to rely on a stable system this is not recommended.
