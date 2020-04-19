---
title: "Iterator implementation has been updated to the latest spec"
date: "2013-10-08T20:15:35-04:00"
categories: ["javascript"]
tags: []
releases: ["27", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=881226"
      title: "Bug 881226 – Change {Array, Map, Set} iterator methods to mach the latest spec"
---
The implementation of the [iterator protocol](https://bugzilla.mozilla.org/show_bug.cgi?id=907077) and [`for...of` loop](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of) has been updated to comply with the ECMAScript 6 spec (moving away from the SpiderMonkey legacy iterator protocol using [`StopIteration`](https://developer.mozilla.org/docs/SpiderMonkey/JSAPI_Reference/JS_ThrowStopIteration)). The `iterator` method of the [`Array`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array), [`Map`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Map), [`Set`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Set) and [`String`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) interfaces has been renamed to `@@iterator`. Previously, the `next` method of an iterator returned a value from the array (or a key-value pair from the object), and raised a `StopIteration` exception when the iteration was done. The `next` method now returns an object like `{ done: false, value: <em>value</em> }` then returns `{ done: true, value: undefined }` when the iteration is done.
