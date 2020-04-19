---
title: "`Blob.mozSlice()` の対応が廃止されました"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
versions: ["30", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=961804"
      title: "Bug 961804 – Drop support for Blob.mozSlice"
---
Firefox 15 以降廃止予定となっていた [`Blob`](https://developer.mozilla.org/docs/Web/API/Blob) オブジェクトの `mozSlice` メソッドが、Firefox 30 で削除されました。代わりに接頭辞なしの `slice` メソッドを使ってください。
