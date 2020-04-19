---
title: "Calling `Map`/`Set`/`WeakMap` without `new` will throw"
date: "2015-08-05T00:48:18-04:00"
categories: ["javascript"]
tags: []
versions: ["42", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083752"
      title: "Bug 1083752 - Calling Map/Set/WeakMap() (without `new`) should throw"
---
As part of the ECMAScript 2015 compliance, Firefox now throws a [`TypeError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/TypeError) if you call one of the [`Map`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Map), [`Set`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Set) or [`WeakMap`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) constructor without using the [`new`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/new) operator.
