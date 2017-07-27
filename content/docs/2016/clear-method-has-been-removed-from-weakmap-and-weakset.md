---
title: "`clear` method has been removed from `WeakMap` and `WeakSet`"
date: "2016-01-12T19:13:00-05:00"
categories: ["javascript"]
tags: []
versions: ["46"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1101817"
      title: "Bug 1101817 - Remove Weak{Map,Set}.prototype.clear"
aliases:
    - "/en-CA/docs/2015/clear-method-will-be-removed-from-weakmap-and-weakset/"
---
The [`WeakMap.prototype.clear`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap/clear) and [`WeakSet.prototype.clear`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakSet/clear) methods have been removed with Firefox 46 since those are no longer a part of the ECMAScript 2015 (ES6) spec. Just use `new WeakMap()` instead to get an empty [`WeakMap`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) object. The same applies to [`WeakSet`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakSet).
