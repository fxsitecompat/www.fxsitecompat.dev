---
title: "`null` iterable for `Map` and `Set` is now ignored instead of throwing"
date: "2015-01-16T09:37:54-05:00"
categories: ["javascript"]
tags: []
versions: ["37"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1092538": "Bug 1092538 – Ignore `null` iterable in Map, Set, WeakMap and WeakSet constructors"
---
The [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map), [`Set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set), [`WeakMap`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) and [`WeakSet`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakSet) constructors no longer throw a [`TypeError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError) when [`null`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/null) is passed as the iterable argument, like `new Map(null)`. Starting with Firefox 37, those constructors just ignore it.
