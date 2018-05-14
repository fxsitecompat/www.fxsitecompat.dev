---
title: "`new` なしで `Proxy` を呼び出した場合に例外が投げられます"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
versions: ["38"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=945566"
      title: "Bug 945566 – ES6 Proxies: calling Proxy() without `new` keyword -> TypeError"
---
Firefox は、仕様に従って、[`new`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/new) 演算子なしに [`Proxy`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy) コンストラクターが呼び出された場合に [`TypeError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/TypeError) を投げるようになりました。
