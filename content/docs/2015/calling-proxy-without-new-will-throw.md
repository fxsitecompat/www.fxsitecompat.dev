---
title: "Calling `Proxy` without `new` will throw"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
versions: ["38"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=945566"
      title: "Bug 945566 – ES6 Proxies: calling Proxy() without `new` keyword -> TypeError"
---
Firefox now throws a [`TypeError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/TypeError) exception when the [`Proxy`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy) constructor is called without the [`new`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/new) operator, as per the spec.
