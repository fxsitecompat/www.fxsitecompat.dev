---
title: "`__defineGetter__` and `__defineSetter__` will be removed"
date: "2015-10-27T23:48:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=647423": "Bug 647423 - Remove __defineGetter__ and __defineSetter__ support"
---
The non-standard, deprecated [`Object.prototype.__defineGetter__`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/__defineGetter__) and [`__defineSetter__`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/__defineSetter__) methods will be removed in the future. Use the standard [`get`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/get), [`set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/set) syntax or [`Object.defineProperty`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty) method instead.
