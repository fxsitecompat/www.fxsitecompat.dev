---
title: "`ArrayBuffer.slice` が削除されました"
date: "2016-12-04T19:50:00-05:00"
categories: ["javascript"]
tags: []
versions: ["53"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1313112"
      title: "Bug 1313112 - Deprecate and remove ArrayBuffer.slice"
aliases:
    - "/ja/docs/2016/arraybuffer-slice-will-be-removed/"
---
[Firefox 52 以降廃止予定となっていた](https://www.fxsitecompat.com/ja/docs/2016/arraybuffer-slice-has-been-deprecated/) 非標準の静的メソッド `ArrayBuffer.slice` は、Firefox 53 で削除されました。標準の [`ArrayBuffer.prototype.slice`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer/slice) メソッドで代用してください。
