---
<!--title: Installation-->
title: インストール
weight: -20
---

<!--This page describes how to install the MATE Desktop Environment.-->
このページでは、MATE デスクトップ環境をインストールする方法について説明します。

{{< toc >}}

<!--## Preinstalled-->
## プリインストール

<!--We recommend to use a distribution that already comes with the MATE Desktop pre-installed, such as (but not limited to):-->
私たちは、すでにMATEデスクトップがインストール済みの Linux ディストリビューション（下記）をお使いになることをお推めします（ただし、それに限定されることはありません）。

### Linux

- [Fedora MATE-Compiz Spin](https://spins.fedoraproject.org/mate-compiz/)
- [Ubuntu MATE](https://ubuntu-mate.org/)
- [Linux Mint - MATE](https://linuxmint.com/edition.php?id=285)
<!--- [Debian](https://www.debian.org/): In the net-install installer choose the "Mate Desktop Environment" option. Alternatively you can use a [live install image](https://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/) (scroll down and choose the iso file with "mate" in its name).-->
- [Debian](https://www.debian.org/): ネットワーク用インストーラを利用する場合は、「Mate デスクトップ環境」というオプションを選択します。また、[Debian live インストールイメージ|live install image](https://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/)を使用することもできます（スクロールダウンして、名前に「mate」が含まれる iso ファイルを選択してください）。
- [Manjaro MATE Community Edition](https://manjaro.org/download/#mate)
- [Solus](https://getsol.us/download/)

<!--If you already have a Linux distribution installed and want to switch to the MATE Desktop without reinstalling everything, this is still possible. Almost every distribution include the MATE Desktop in their official repositories.-->
すでに Linux ディストリビューションがインストールされていて、すべて再インストールすることなく MATE デスクトップに切り替えたい場合にも、これらのディストリビューションでは利用可能です。ほとんどのディストリビューションは公式のリポジトリに MATE デスクトップを用意しています。

### BSD

<!--- [live install image](https://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/)A simple desktop-oriented operating system based on FreeBSD with MATE.-->
- [live install image](https://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/) FreeBSD をベースに MATE を搭載したシンプルなデスクトップ向けオペレーティングシステムです。

### Illumos

-[openIndiana](https://www.openindiana.org/download/)

<!--## Manual installation-->
## マニュアル・インストール

<!--We now describe how to install the MATE Desktop manually from the official repositories of your distribution. The manual install is useful, if you have a distribution without a graphical interface and decided to use the MATE Desktop.-->
ここでは、ディストリビューションの公式リポジトリから MATE デスクトップを手動（マニュアル）でインストールする方法について説明します。マニュアル・インストールは、グラフィカルインターフェースを持たないディストリビューションで、MATE デスクトップを使用したい場合に便利です。


{{< hint danger >}}
<!--**Manual install**\-->
**マニュアル・インストール
<!--If you already have a Desktop Environment installed (like Gnome, KDE, ...) and install MATE on top of that, there can be conflicting programs (window manager, screensaver, control centre, ...). You can try to remove the old Desktop Environment, but keep in mind that this is not the recommended way to get the best MATE experience.-->
すでにデスクトップ環境（Gnome、KDE など）をインストールしていて、その上 に MATE をインストールした場合、競合するプログラム（ウィンドウマネージャ、スクリーンセーバー、コントロールセンターなど）が存在する可能性があります。古いデスクトップ環境を削除することは可能ですが、MATE デスクトップを最良の状態で使用するためには推奨されない方法であることに注意してください。
{{< /hint >}}

{{< tabs "manual-install" >}}
{{< tab "Debian/Ubuntu/Linux Mint" >}}
<!--Install the MATE Desktop Environment with-->
MATE デスクトップ環境は端末から以下のコマンドでインストールします。

- `sudo apt install mate-desktop-environment`

<!--If you want some extras (such as a menu-editor) you can replace the above command with-->
メニューエディタなど複数の追加機能が必要な場合は、上記のコマンドを次のように置き換えることができます。

- `sudo apt install mate-desktop-environment-extras`

You can still install the extras later on if you are not sure about it right now.
今は未だよく分からないないという方は、後から一連のアプリケーション (Extras) を追加することができます。

<!--If you do not have a desktop environment installed already you might want to install a graphical [display manager](https://wiki.archlinux.org/title/Display_manager).-->
デスクトップ環境を未だインストールしていない場合は、グラフィカルなディスプレイ・マネージャーをインストールすることをお推めします。

<!--For example you can use  [LightDM](https://wiki.archlinux.org/title/LightDM):-->
たとえば、あなたが [LightDM](https://wiki.archlinux.org/title/LightDM) を使いたいときは次のようにしてインストールします。

- `sudo apt install lightdm lightdm-gtk-greeter`

<!--After rebooting you should be able to login to the MATE Desktop.-->
再起動後、MATE デスクトップにログインできるようになるはずです。

<!--If you do not want a display manager, you can add mate-session to `~/.xinitrc` file.-->
ディスプレイマネージャーが不要な場合は、 `~/.xinitrc` ファイルに mate-session を追加してください。

```
exec ck-launch-session mate-session
```
<!--Now can type `startx`.-->
これで `startx` と入力できるようになります。

{{< hint info >}}
<!--If you have authorization problems (e.g. when mounting disks), try adding `dbus-launch` after `ck-launch-session`.-->
もし、認証に問題がある場合 (例えば、ディスクをマウントする時)、 `ck-launch-session` の後に `dbus-launch` を追加してみてください。

{{< /hint >}}

{{< /tab >}}

{{< tab "Fedora" >}}
<!--Install the MATE Desktop Environment with-->
MATE デスクトップ環境をインストールするには、次のコマンドです。

- `sudo dnf install mate-desktop-environment`
{{< /tab >}}

{{< tab "Arch/Manjaro" >}}
<!--Install the MATE Desktop Environment with-->
MATE デスクトップ環境をインストールするには、次のコマンドです。

- `sudo pacman -Sy mate-desktop-environment`
{{< /tab >}}

{{< tab "Solus" >}}
<!--Install the MATE Desktop Environment with
MATE デスクトップ環境をインストールするには、次のコマンドです。-->

- `sudo eopkg it -c desktop.mate`
{{< /tab >}}
{{< /tabs >}}
