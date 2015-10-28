---
title: "`__defineGetter__` と `__defineSetter__` が削除されます"
date: "2015-10-27T23:48:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=647423": "Bug 647423 - Remove __defineGetter__ and __defineSetter__ support"
---
非標準で廃止予定となっている [`Object.prototype.__defineGetter__`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/__defineGetter__)、[`__defineSetter__`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/__defineSetter__) 両メソッドは、将来的に削除されます。標準の [`get`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Functions/get)、[`set`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Functions/set) 構文、あるいは [`Object.defineProperty`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty) メソッドで代用してください。
