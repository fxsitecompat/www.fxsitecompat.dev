---
title: "`ArrayBuffer.slice` が廃止予定となりました"
date: "2016-11-16T19:34:00-05:00"
categories: ["javascript"]
tags: []
versions: ["52"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1313112"
      title: "Bug 1313112 - Deprecate and remove ArrayBuffer.slice"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1316913"
      title: "Bug 1316913 - Warn about ArrayBuffer.slice"
---
非標準の静的メソッド `ArrayBuffer.slice` が廃止予定とされ、Firefox 53 で削除されることとなりました。標準の [`ArrayBuffer.prototype.slice`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer/slice) メソッドで代用してください。
