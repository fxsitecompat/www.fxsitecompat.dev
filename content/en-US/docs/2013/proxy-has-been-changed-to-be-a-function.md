---
title: "`Proxy` has been changed to be a function"
date: "2013-07-14T19:12:37-04:00"
categories: ["javascript"]
tags: []
versions: "25"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=788172": "Bug 788172 – Proxy is not a function (typeof Proxy should be \'function\')"
---
The [`Proxy`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy) interface has been changed from an object to a function, and now it's callable without the [`new`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new) operator. You may have to care about this if you are using the [`typeof`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof) operator for a feature detection, as `typeof Proxy` returns `"function"`.
