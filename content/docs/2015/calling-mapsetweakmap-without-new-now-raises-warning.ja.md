---
title: "`new` なしで `Map`/`Set`/`WeakMap` を呼び出した場合に警告が表示されるようになりました"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
releases: ["38", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1062075"
      title: "Bug 1108930 – Throw for ES6 built-in constructors called without `new`"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1108930"
      title: "Bug 1108930 – Fix in-tree consumers that call Map/Set/WeakMap constructors without \"new\""
---
Firefox は近く、ECMAScript 6 仕様に従って、[`new`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/new) 演算子なしに [`Map`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Map)、[`Set`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Set) あるいは [`WeakMap`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) コンストラクターが呼び出された場合に [`TypeError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/TypeError) を投げるようになります。Firefox 38 は、そうしたコードを見つけた場合に [ウェブコンソール](https://developer.mozilla.org/docs/Tools/Web_Console) に警告を出力します。
