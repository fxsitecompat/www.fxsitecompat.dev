---
title: "`atob` が空白を無視するようになりました"
date: "2013-10-08T20:15:35-04:00"
categories: ["dom"]
tags: []
versions: ["27"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=711180"
      title: "Bug 711180 – atob should ignore whitespace"
---
Base64 エンコードされた文字列をデコードする [`window.atob`](https://developer.mozilla.org/docs/Web/API/window.atob) メソッドが最新の HTML5 仕様に準拠するため更新され、引数内のすべての空白文字を無視するようになりました。
