---
title: Installation
weight: -20
---

This page describes how to install the MATE Desktop Environment.

{{< toc >}}

## Preinstalled

We recommend to use a distribution that already comes with the MATE Desktop pre-installed, such as (but not limited to):

- [Fedora MATE-Compiz Spin](https://spins.fedoraproject.org/mate-compiz/)
- [Ubuntu MATE](https://ubuntu-mate.org/)
- [Linux Mint - MATE](https://linuxmint.com/edition.php?id=285)
- [Debian](https://www.debian.org/): In the net-install installer choose the "Mate Desktop Environment" option. Alternatively you can use a [live install image](https://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/) (scroll down and choose the iso file with "mate" in its name).
- [Manjaro MATE Community Edition](https://manjaro.org/download/#mate)

If you already have a Linux distribution installed and want to switch to the MATE Desktop without reinstalling everything, this is still possible. Almost every distribution include the MATE Desktop in their official repositories.

## Manual installation

We now describe how to install the MATE Desktop manually from the official repositories of your distribution. The manual install is useful, if you have a distribution without a graphical interface and decided to use the MATE Desktop.

{{< hint danger >}}
**Manual install**\
If you already have a Desktop Environment installed (like Gnome, KDE, ...) and install MATE on top of that, there can be conflicting programs (window manager, screensaver, control centre, ...). You can try to remove the old Desktop Environment, but keep in mind that this is not the recommended way to get the best MATE experience.
{{< /hint >}}

{{< tabs "manual-install" >}}
{{< tab "Debian/Ubuntu/Linux Mint" >}}
Install the MATE Desktop Environment with

- `sudo apt install mate-desktop-environment`

If you want some extras (such as a menu-editor) you can replace the above command with

- `sudo apt install mate-desktop-environment-extras`

You can still install the extras later on if you are not sure about it right now.

If you do not have a desktop environment installed already you might want to install a graphical [display manager](https://wiki.archlinux.org/title/Display_manager).

For example you can use  [LightDM](https://wiki.archlinux.org/title/LightDM):

- `sudo apt install lightdm lightdm-gtk-greeter`

After rebooting you should be able to login to the MATE Desktop.

If you do not want a display manager, you can add mate-session to `~/.xinitrc` file.

```
exec ck-launch-session mate-session
```
Now can type `startx`.

{{< hint info >}}
If you have authorization problems (e.g. when mounting disks), try adding `dbus-launch` after `ck-launch-session`.

{{< /hint >}}

{{< /tab >}}

{{< tab "Fedora" >}}
Install the MATE Desktop Environment with

- `sudo dnf install mate-desktop-environment`
{{< /tab >}}

{{< tab "Arch/Manjaro" >}}
Install the MATE Desktop Environment with

- `sudo pacman -Sy mate-desktop-environment`
{{< /tab >}}
{{< /tabs >}}
