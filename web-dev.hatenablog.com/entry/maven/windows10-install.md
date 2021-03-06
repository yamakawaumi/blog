---
Title: Maven：Win10にインストール
Category:
- Maven
Date: 2017-06-10T09:02:37+09:00
URL: http://web-dev.hatenablog.com/entry/maven/windows10-install
EditURL: https://blog.hatena.ne.jp/mamorums/web-dev.hatenablog.com/atom/entry/13355765958053917957
---

Maven を Windows10 64bit にインストールする手順を書いていきます。


## 前提
Windows10 に [JDK をインストール](/entry/java/jdk/8/windows10-install)して、[環境変数を設定](/entry/java/jdk/8/windows10-env-variables) していることが前提になります。


## 手順1. ダウンロード
[Maven のダウンロードページ](https://maven.apache.org/download.cgi) から、安定版の「Binary Zip archive」をダウンロードします。記事作成日（2017.06.10）の安定版は 3.5.0 で、ファイル名は `apache-maven-3.5.0-bin.zip` でした。


## 手順2. 解凍
ダウンロードしたら、Zip を好きな場所（例：`C:\opt\apache-maven-3.5.0`）に解凍します。

[f:id:mamorums:20170610090140p:plain]


## 手順3. 環境変数 Path の設定
Maven の binフォルダ（例：`C:\opt\apache-maven-3.5.0\bin`）を、環境変数 `Path` に追加します。

[f:id:mamorums:20170610090153p:plain]


## 手順4. 動作確認（任意）
コマンドプロンプトで `mvn -v` を実行します。Maven のバージョン等が表示されれば成功です。

```txt
> mvn -v
Apache Maven 3.5.0 ...省略
```
