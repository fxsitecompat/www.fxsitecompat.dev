---
title: "Calling typed array constructors without `new` will throw"
date: "2015-10-14T16:00:00-07:00"
categories: ["javascript"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=980945": "Bug 980945 - Typed array constructors should not work without \"new\" per spec"
---
As part of the ECMAScript 2015 (ES6) compliance, Firefox now throws a [`TypeError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError) if [typed array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Typed_arrays) constructors, including [`Uint8Array`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array), [`Int16Array`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Int16Array) and [`Float64Array`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Float64Array), are called without using the [`new`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new) operator.
