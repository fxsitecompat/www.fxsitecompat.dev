---
title: "Returning non-object value from `iterator.next()` will throw"
date: "2016-08-14T16:17:00-04:00"
categories: ["javascript"]
tags: []
versions: ["51", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1016936"
      title: "Bug 1016936 - Iteration: throw if the value returned by iterator.next() is not an object"
aliases:
    - "/en-CA/docs/2016/retuning-non-object-value-by-iterator-next-will-throw/"
---
In the [iterator protocol](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Iteration_protocols#iterator), the `next` method always has to return an object with appropriate properties including `done` and `value`. Firefox now throws a `TypeError` when a non-object value such as `false` or `undefined` is returned from a developer-defined `next` method, according to the ECMAScript 2015 (ES6) spec.
