---
title: "`WeakMap` implementation has been updated"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
releases: ["38", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1009349"
      title: "Bug 1009349 – Deprecate optional second argument to WeakMap.prototype.get"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1127827"
      title: "Bug 1127827 – WeakMap.get, has and delete should not throw when key param is not an object"
---
The implementation of [`WeakMap`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) has been updated for the latest spec, and the optional second fallback argument of the [`get`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap/get) method has been removed. Also, the [`get`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap/get), [`has`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap/has) and [`delete`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap/delete) methods now return [`undefined`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/undefined) instead of throwing a [`TypeError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/TypeError) when the key argument is not an object or cannot be found.
