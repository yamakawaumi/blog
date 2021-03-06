---
Title: Gradle：CentOSにインストール
Category:
- Gradle
Date: 2016-05-14T12:20:00+09:00
URL: http://web-dev.hatenablog.com/entry/gradle/centos-install
EditURL: https://blog.hatena.ne.jp/mamorums/web-dev.hatenablog.com/atom/entry/10328749687179308965
---

Gradle を CentOS にインストールする手順を書いていきます。手順は、[JDK がインストール](/entry/java/jdk/centos-install) されていることが前提となります。


## 手順1. ダウンロード
root でインストール先（例：`/opt`）に移動します。それから、`wget` でダウンロードします。

```txt
# cd /opt
# wget https://services.gradle.org/distributions/gradle-2.13-bin.zip
```

`wget` の引数（ダウンロードURL）は、[Gradle ダウンロードページ](http://gradle.org/gradle-download/) で確認できます。


## 手順2. 解凍
ダウンロードした圧縮ファイルを解凍します。

```
# unzip gradle-2.13-bin.zip
```

解凍が終わったら、圧縮ファイルは削除しても大丈夫です。

```
# rm gradle-2.13-bin.zip
```


## 手順3. .bash_profile の編集
Gradle を使うユーザになって、vi 等で `~/.bash_profile` を開きます。それから、ファイル末尾に次の設定を追加します。

`追加`

```
export JAVA_HOME=/usr/java/jdk1.8.0_77
export PATH=$PATH:/opt/gradle-2.13/bin
```

`JAVA_HOME` は、環境に応じた値を設定します（設定済みなら不要）。


## 手順4. 環境変数の反映
次のコマンドで、追加した環境変数を読み込みます。

```
$ source ~/.bash_profile
```

次回ログイン時は、自動で反映されます。


## 手順5. 確認
次のコマンドを実行して、Gradle のバージョンが表示されれば大丈夫です。

```
$  gradle -v

------------------------------------------------------------
Gradle 2.13
------------------------------------------------------------

Build time:   2016-04-25 04:10:10 UTC
・・・省略・・・
```
