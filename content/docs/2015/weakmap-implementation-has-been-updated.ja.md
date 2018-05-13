---
title: "`WeakMap` 実装が更新されました"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
versions: ["38"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1009349"
      title: "Bug 1009349 – Deprecate optional second argument to WeakMap.prototype.get"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1127827"
      title: "Bug 1127827 – WeakMap.get, has and delete should not throw when key param is not an object"
---
[`WeakMap`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) の実装が最新の仕様に合わせて更新され、オプションとして指定可能だった [`get`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap/get) メソッドの 2 番目のフォールバック引数が削除されました。また、[`get`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap/get)、[`has`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap/has)、[`delete`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap/delete) の各メソッドが、キー引数がオブジェクトでなかった場合や見つからなかった場合に、[`TypeError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/TypeError) を投げる代わりに [`undefined`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/undefined) を返すようになりました。
