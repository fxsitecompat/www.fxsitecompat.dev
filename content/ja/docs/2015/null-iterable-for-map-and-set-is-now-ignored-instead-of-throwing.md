---
title: "`Map` と `Set` の `null` 引数が例外を投げる代わりに無視されるようになりました"
date: "2015-01-16T09:37:54-05:00"
categories: ["javascript"]
tags: []
versions: ["37"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1092538": "Bug 1092538 – Ignore `null` iterable in Map, Set, WeakMap and WeakSet constructors"
---
[`Map`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Map)、[`Set`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Set)、[`WeakMap`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/WeakMap)、[`WeakSet`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/WeakSet) の各コンストラクタが、`new Map(null)` のように `iterable` 引数として [`null`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/null) が渡されても [`TypeError`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/TypeError) を投げなくなりました。Firefox 37 以降、それらのコンストラクタは単に `null` を無視します。
