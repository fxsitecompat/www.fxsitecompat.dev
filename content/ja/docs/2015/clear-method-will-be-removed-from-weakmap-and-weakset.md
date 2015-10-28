---
title: "`WeakMap`、`WeakSet` から `clear` メソッドが削除されます"
date: "2015-10-28T00:10:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1101817": "Bug 1101817 - Remove Weak{Map,Set}.prototype.clear"
---
[`WeakMap.prototype.clear`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/WeakMap/clear)、[`WeakSet.prototype.clear`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/WeakSet/clear) 両メソッドは、ECMAScript 2015 (ES6) 仕様から外れたため、近い将来削除されます。空の [`WeakMap`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) オブジェクトを得るには単に `new WeakMap()` を使ってください。[`WeakSet`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/WeakSet) についても同じことが当てはまります。
