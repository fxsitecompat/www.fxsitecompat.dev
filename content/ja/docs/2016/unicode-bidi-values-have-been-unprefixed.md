---
title: "`unicode-bidi` の値から接頭辞が外れました"
date: "2016-07-04T14:29:00-04:00"
categories: ["css"]
tags: []
versions: ["50"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1141895"
      title: "Bug 1141895 - Unprefix values of unicode-bidi"
---
[`unicode-bidi`](https://developer.mozilla.org/ja/docs/Web/CSS/unicode-bidi) CSS プロパティの接頭辞付き値、つまり `-moz-isolate`、`-moz-isolate-override`、`-moz-plaintext` が、ベンダー接頭辞なしに使えるようになりました。接頭辞付き値への対応は将来的に削除されます。
