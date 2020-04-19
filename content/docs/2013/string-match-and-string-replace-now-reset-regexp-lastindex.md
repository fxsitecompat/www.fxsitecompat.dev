---
title: "`String.match()` and `String.replace()` now reset `RegExp.lastIndex`"
date: "2013-10-08T20:15:35-04:00"
categories: ["javascript"]
tags: []
releases: ["27", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=501739"
      title: "Bug 501739 – String match and replace methods do not update global regexp lastIndex per ES3&5"
---
The [`String.match`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/match) and [`String.replace`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/replace) methods have been refactored to resolve a spec conformance issue on [`RegExp.lastIndex`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp/lastIndex). When those methods are called with a global regular expression, the `lastIndex`, if specified, will be reset to `0`.
