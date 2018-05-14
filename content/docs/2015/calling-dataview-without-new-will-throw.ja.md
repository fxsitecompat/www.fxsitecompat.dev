---
title: "`new` なしの `DataView` 呼び出しが例外を投げるようになりました"
date: "2015-04-27T13:17:23-04:00"
categories: ["javascript"]
tags: []
versions: ["40"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1142279"
      title: "Bug 1142279 – DataView should require `new`"
---
[`DataView`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/DataView) コンストラクターが [`new`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/new) 演算子なしに呼び出された場合、Firefox は仕様に従って [`TypeError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/TypeError) 例外を投げるようになりました。
