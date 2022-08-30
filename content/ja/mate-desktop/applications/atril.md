---
title: Atril - PDF ビューア
weight: -20
---

<span class="badge-placeholder">[![Build Status](https://travis-ci.org/mate-desktop/atril.svg?branch=master)](https://travis-ci.org/github/mate-desktop/mate-desktop)</span>
<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/mate-desktop/atril)](https://github.com/mate-desktop/mate-desktop/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/mate-desktop/atril)](https://github.com/mate-desktop/atril/graphs/contributors)</span>
<span class="badge-placeholder">[![License](https://img.shields.io/github/license/mate-desktop/atril)](https://github.com/mate-desktop/atril/blob/main/LICENSE)</span>

[Source Code](https://github.com/mate-desktop/atril) | [Bug Tracker](https://github.com/mate-desktop/atril/issues) | [Dependencies](https://github.com/mate-desktop/atril/blob/master/.build.yml)

![](https://raw.githubusercontent.com/mate-desktop/atril/master/data/icons/scalable/apps/atril.svg)

{{< columns >}}
Atril は、MATE デスクトップ環境の公式な文書ビューアです。
シンプルなマルチページ対応の文書ビューアです。ポストスクリプト (PS), エンカプセレーティド・ポストスクリプト (EPS)、
 DJVU、DVI、XPS、ポータブル・ドキュメント・フォーマット (PDF) といった各種形式のファイルを表示、印刷することができます。

対象とする文書が技術的にサポートされている場合には、テキストの検索も可能です。
クリップボードへのコピー、HTML 上での移動、目次のブックマークも可能です。

    <--->

![](/img/applications/atril-window.png)

{{< /columns >}}



{{< expand "More">}}

シンタックス（構文）

       atril [OPTIONS...] [FILES...]

オプション

       filename(s)...
              Atril の起動時に開くファイルを指定します。ファイルを指定しない場合、Atril は
                 空白のウィンドウで起動するので、メニューから、または CTRL + O のショートカット
                 でファイルを開くことができます。スペースで区切れば、複数のファイルを読み込むこと
                 ができます。Atril はリモートファイルの処理もサポートします。

       -p, --page-label=PAGE
                 これでページラベルを指定すると、そのページが文書内に存在する場合、選択できます。

       -i, --page-index=NUMBER
                 これでページ番号を指定すると、そのページが存在する場合、選択できます。

       -f, --fullscreen
              Atril を全画面モードで起動します。全画面モードで起動するには、文書を指定する
                 必要があります。

       -s, --presentation
              Atril をプレゼンテーションモードで起動します。このモードで起動するには、文書
                 を指定する必要があります。

       -w, --preview
              Atril をプレビューモードで起動します。このモードで起動するには、文書を指定す
                 る必要があります。

       --display=DISPLAY
                 使用する X ディスプレイ。

       --version
                 バージョン情報を出力して終了します。

       -?, -h, --help
                 標準的なコマンドラインオプションを表示します。

       --help-all
                 すべてのコマンドラインオプションを表示します。

       このプログラムでは、GTK の標準的なオプションも使用できます。

{{< /expand >}}

## ビルド / インストール

シンプルなビルド方法:

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

