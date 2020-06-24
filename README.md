これは A Tour of Go の簡易HTML版を生成するためのリポジトリです。
生成物は `html` ディレクトリ以下にあります。

## 生成方法のメモ

```sh
$ present -play=false
```

でサーバーを立てておき、別のシェルから

```sh
$ cd html
$ wget localhost:3999/content/{basics,concurrency,flowcontrol,methods,moretypes}.article
$ rename s/article/html/ *.article
$ wget localhost:3999/static/article.css
$ sed -i -e 's/\/static\/article.css/article.css/g' *.html
```

あとは article.css をいいかんじに編集する。

-------

A Tour of Go is an introduction to the Go programming language.

The easiest way to install the tour locally is to install
[a binary release of Go](https://golang.org/dl/) and then run:

	$ go tool tour

To install the tour from source, first 
[set up a workspace](https://golang.org/doc/code.html) and then run:

	$ go get github.com/atotto/go-tour-jp/gotour

This will place a `gotour` binary in your workspace's `bin` directory.

Unless otherwise noted, the go-tour source files are distributed
under the BSD-style license found in the LICENSE file.

Contributions should follow the same procedure as for the Go project:
https://golang.org/doc/contribute.html
