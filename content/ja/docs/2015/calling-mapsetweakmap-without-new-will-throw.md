---
title: "`new` なしで `Map`/`Set`/`WeakMap` を呼び出すと例外が投げられます"
date: "2015-08-05T00:48:18-04:00"
categories: ["javascript"]
tags: []
versions: ["42"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083752"
      title: "Bug 1083752 - Calling Map/Set/WeakMap() (without `new`) should throw"
---
ECMAScript 2015 準拠の一環として、[`new`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/new) 演算子なしで [`Map`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Map)、[`Set`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Set) あるいは [`WeakMap`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) コンストラクターが呼び出された場合に、Firefox は [`TypeError`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/TypeError) を投げるようになりました。
