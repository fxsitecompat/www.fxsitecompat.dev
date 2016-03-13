---
title: "`__defineGetter__` and `__defineSetter__` can no longer be called at the global scope"
date: "2016-03-12T19:11:00-05:00"
categories: ["javascript"]
tags: []
versions: ["48"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1253016": "Bug 1253016 - Remove legacy __defineGetter__/__defineSetter__ this behavior"
---
Previously, the [`__defineGetter__`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/__defineGetter__) and [`__defineSetter__`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/__defineSetter__) methods could be called at the global scope without any object. Firefox 48 and later will throw such code since the legacy behaviour, where the associated object becomes `null` or `undefined`, is not allowed by ECMAScript 7. The workaround is to use `this.__defineGetter__` or `this.__defineSetter__`.
