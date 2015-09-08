---
title: "Calling `Map`/`Set`/`WeakMap` without `new` now raises warning"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
versions: "38"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1062075": "Bug 1108930 – Throw for ES6 built-in constructors called without `new`"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1108930": "Bug 1108930 – Fix in-tree consumers that call Map/Set/WeakMap constructors without \"new\""
---
Firefox will soon throw a [`TypeError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError) exception when the [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map), [`Set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set), or [`WeakMap`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) constructor is called without the [`new`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new) operator, as per the ECMAScript 6 spec. Starting with Firefox 38, the [Web Console](https://developer.mozilla.org/en-US/docs/Tools/Web_Console) shows a warning for such use cases.
