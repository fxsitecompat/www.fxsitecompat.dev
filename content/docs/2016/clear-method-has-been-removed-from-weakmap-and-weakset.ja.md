---
title: "`WeakMap`、`WeakSet` から `clear` メソッドが削除されました"
date: "2016-01-12T19:13:00-05:00"
categories: ["javascript"]
tags: []
versions: ["46"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1101817"
      title: "Bug 1101817 - Remove Weak{Map,Set}.prototype.clear"
aliases:
    - "/ja/docs/2015/clear-method-will-be-removed-from-weakmap-and-weakset/"
---
[`WeakMap.prototype.clear`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap/clear)、[`WeakSet.prototype.clear`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakSet/clear) 両メソッドは、ECMAScript 2015 (ES6) 仕様から外れたため、Firefox 46 で削除されました。空の [`WeakMap`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) オブジェクトを得るには単に `new WeakMap()` を使ってください。[`WeakSet`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakSet) についても同じことが当てはまります。
