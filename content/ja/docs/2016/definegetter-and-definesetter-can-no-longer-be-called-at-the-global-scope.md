---
title: "`__defineGetter__` や `__defineSetter__` をグローバルスコープで呼び出すことはできなくなりました"
date: "2016-03-12T19:11:00-05:00"
categories: ["javascript"]
tags: []
versions: ["48"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1253016": "Bug 1253016 - Remove legacy __defineGetter__/__defineSetter__ this behavior"
---
従来、[`__defineGetter__`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/__defineGetter__)、[`__defineSetter__`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/__defineSetter__) 両メソッドは、グローバルスコープでオブジェクト抜きに呼び出すことが可能でした。関連付けられたオブジェクトが `null` あるいは `undefined` となるこの古い挙動は ECMAScript 7 では認められていないため、Firefox 48 以降ではそうしたコードに対して例外が投げられます。回避策は、`this.__defineGetter__` か `this.__defineSetter__` を使うことです。
