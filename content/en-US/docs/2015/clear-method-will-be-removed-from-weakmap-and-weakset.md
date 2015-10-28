---
title: "`clear` method will be removed from `WeakMap` and `WeakSet`"
date: "2015-10-28T00:10:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1101817": "Bug 1101817 - Remove Weak{Map,Set}.prototype.clear"
---
The [`WeakMap.prototype.clear`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap/clear) and [`WeakSet.prototype.clear`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakSet/clear) methods will be removed in the near future since those are no longer a part of the ECMAScript 2015 (ES6) spec. Just use `new WeakMap()` instead to get an empty [`WeakMap`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) object. Same applies to [`WeakSet`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakSet).
