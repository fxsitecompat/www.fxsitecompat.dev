---
title: "`Number` supports binary and octal literals"
date: "2014-12-19T11:15:21-05:00"
categories: ["javascript"]
tags: []
versions: ["36"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1079120"
      title: "Bug 1079120 – Make ToNumber(string) support binary and octal literals"
---
The [`Number`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number) object now supports binary and octal literals as per the new ECMAScript 6 draft, so `Number('0b11')` and `Number('0o77')`, both returned [`NaN`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/NaN) before, will return `3` and `63` respectively.
