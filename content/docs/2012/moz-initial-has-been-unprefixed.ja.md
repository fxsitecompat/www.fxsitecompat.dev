---
title: "`-moz-initial` の接頭辞が外れました"
date: "2012-12-03T03:54:45-05:00"
categories: ["css"]
tags: []
versions: ["19"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=806068"
      title: "Bug 806068 – Unprefix -moz-initial"
---
`-moz-initial` キーワードの接頭辞が外れました。`-moz-initial` は当面 [`initial`](https://developer.mozilla.org/ja/docs/CSS/initial) のエイリアスとして残されますが、[いずれ削除されます](https://bugzilla.mozilla.org/show_bug.cgi?id=807184) ので、今後は接頭辞なしのキーワードを使用してください。
