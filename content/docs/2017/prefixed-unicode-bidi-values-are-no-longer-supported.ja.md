---
title: "接頭辞付き `unicode-bidi` 値への対応が打ち切られました"
date: "2017-02-09T03:55:00-05:00"
categories: ["css"]
tags: []
versions: ["54", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1333675"
      title: "Bug 1333675 - Consider removing prefixed value of unicode-bidi"
---
[Firefox 50](https://www.fxsitecompat.dev/ja/docs/2016/unicode-bidi-values-have-been-unprefixed/) 以降廃止予定となっていたベンダー接頭辞付き [`unicode-bidi`](https://developer.mozilla.org/docs/Web/CSS/unicode-bidi) CSS プロパティ値への対応は、Firefox 54 で削除されました。`-moz-isolate`、`-moz-isolate-override`、`-moz-plaintext` の代わりに接頭辞なしの値を使用してください。
