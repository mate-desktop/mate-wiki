---
title: Caja - ファイルマネージャ
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/caja.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/caja)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/caja)](https://github.com/mate-desktop/caja/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/caja)](https://github.com/mate-desktop/caja/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/caja) | [Bug Tracker](https://github.com/mate-desktop/caja/issues) | [Dependencies](https://github.com/mate-desktop/caja/blob/master/.build.yml)

![](https://raw.githubusercontent.com/mate-desktop/mate-icon-theme/master/mate/48x48/apps/system-file-manager.png)

{{< columns >}}

Caja は MATE デスクトップ環境において標準のファイルマネージャです。これを使うことによって、ファイルやディレクトリの管理、操作、カスタマイズが簡単にできます。Caja は、SSH、FTP、WebDav (HTTP/HTTPS) など、ローカルおよびリモートのファイルシステムにアクセスすることができます。

また、Caja はデスクトップの背景や、リンク、アプリケーションの起動に使用するアイコンを提供します。ファイル、ディレクトリ、ゴミ箱、CD/DVD/BD や USB ドライブなどのリムーバブルメディアへのアクセスも提供します。

    <--->

![](/img/applications/caja-window.png)

{{< /columns >}}


{{< expand "More">}}

SYNOPSIS

       caja [OPTIONS...] [URI...]

OPTIONS

       --browser
              ブラウザのウィンドウを開きます。

       -c, --check
              セルフチェックテストのクイックセットを実行します。

       --display=DISPLAY
              使用する X ディスプレイ。

       -g, --geometry=GEOMETRY
              与えられたジオメトリで初期ウィンドウを作成します。

       -t, --tabs
              URI をタブで開きます。

       -n, --no-default-window
              明示的に指定されたURIについてのみウィンドウだけを作成します。

       --no-desktop
              デスクトップを管理しない（環境設定ダイアログで設定した設定を無視します）。

       --force-desktop
              事前設定や環境とは関係なしにデスクトップを管理する（新規起動時のみ)

       -q, --quit
              Caja の使用を中止します。　

       --version
              現在のバージョン情報を表示して終了します。

       -?, -h, --help
              標準的なコマンドラインオプションを表示します。

       --help-all
              すべてのコマンドラインオプションを表示します。

       このプログラムでは、GTK の標準的なオプションも使用できます。

{{< /expand >}}

## ビルド / インストール

シンプルなビルドの方法:

```
$ git submodule update --init --recursive   # Git サブモジュールの初期化
$ ./autogen.sh --prefix=/usr                # ビルドの設定
$ make                                      # ビルド
```
別のプリフィックスにインストールする場合は、上記の `./autogen.sh` コマンドを次のように変更します。

```
$ ./autogen.sh --prefix=/an/other/path
```

パッケージのビルドが完了したら、次のようにしてインストールすることができます。

```
[ 必要に応じて root になってください ]
$ make install                              # インストール
```

