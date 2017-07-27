---
title: "`__defineGetter__` and `__defineSetter__` can no longer be called at the global scope"
date: "2016-03-12T19:11:00-05:00"
categories: ["javascript"]
tags: []
versions: ["48"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1253016"
      title: "Bug 1253016 - Remove legacy __defineGetter__/__defineSetter__ this behavior"
---
Previously, the [`__defineGetter__`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/__defineGetter__) and [`__defineSetter__`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/__defineSetter__) methods could be called at the global scope without any object, because the global object was automatically used in such cases. As part of the ECMAScript 2016 (ES7) compliance, Firefox 48 and later no longer support the legacy behaviour and throw a `TypeError` instead. The workaround here is to explicitly use the [`this`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this) keyword, like `this.__defineGetter__` or `this.__defineSetter__`.
