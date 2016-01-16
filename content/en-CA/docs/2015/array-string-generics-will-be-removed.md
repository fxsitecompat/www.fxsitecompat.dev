---
title: "`Array`/`String` generics will be removed"
date: "2015-11-06T16:08:00-08:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1222547": "Bug 1222547 - Remove Array generics"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1222552": "Bug 1222552 - Remove String generics"
---
The non-standard [`Array` generic methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Array_generic_methods) and [`String` generic methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#String_generic_methods), introduced with [JavaScript 1.6](https://developer.mozilla.org/en-US/docs/Web/JavaScript/New_in_JavaScript/1.6), will be removed in the future.

The [spread operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_operator) can be used as a simple alternative to `Array` generics. For example, `Array.every(str, callback)` can be replaced with `[...str].every(callback)`.

The [`String`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) global object can be used as a simple alternative to `String` generics. For example, `String.replace(num, search, replace)` can be replaced with `String(num).replace(search, replace)`.
