---
title: "`toLocaleString` may return different values than before"
date: "2014-02-07T11:57:09-05:00"
categories: ["javascript"]
tags: []
versions: ["29"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=837963"
      title: "Bug 837963 – [meta] Implement ECMAScript Internationalization API"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=769871"
      title: "Bug 769871 – Reimplement String.localeCompare, Number.toLocaleString, Date.toLocaleString per ECMA-402"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=999003"
      title: "Bug 999003 – toLocaleString with undefined locale uses localized digits specified by the OS"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1010535"
      title: "Bug 1010535 – (new Date()).toLocaleString() changed format"
---
The [`Date.toLocaleString`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleString), [`Date.toLocaleDateString`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString), [`Date.toLocaleTimeString`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleTimeString), [`Number.toLocaleString`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number/toLocaleString) and [`String.localeCompare`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/localeCompare) methods have been reimplemented to support the ECMAScript Internationalization API. Those methods are implementation-dependent if the arguments are omitted, thus results you'll get might be different than the value returned by the previous versions of Firefox.

Formerly, `Date.toLocaleString`, `Date.toLocaleDateString` and `Date.toLocaleTimeString` returned the system date and time, but now the format is different depending on the browser locale. `Number.toLocaleString` will return localized digits defined by the OS, while the previous versions of Firefox returned English digits. `String.localeCompare` may return `1` or `-1` where previously `2` or `-2` was returned.
