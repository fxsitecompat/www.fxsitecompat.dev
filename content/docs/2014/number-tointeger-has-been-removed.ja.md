---
title: "`Number.toInteger()` が削除されました"
date: "2014-07-22T05:06:26-04:00"
categories: ["javascript"]
tags: []
versions: ["33", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1022396"
      title: "Bug 1022396 – remove Number.toInteger"
---
Firefox 16 で実装された [`Number.toInteger`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number/toInteger) メソッドが、ES6 仕様草案から除かれたため、削除されました。ほとんどの場合 [`Number.parseInt`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number/parseInt) で代用可能です。
