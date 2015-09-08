---
title: "`Proxy` handers may throw under specific conditions"
date: "2015-03-17T14:02:59-04:00"
categories: ["javascript"]
tags: []
versions: "39"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1132522": "Bug 1132522 - Treat false return value from certain Proxy handler methods as failure"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=828137": "Bug 828137 - Need APIs that would allow proxies to implement Reject in spec terms"
---
The implementation of the [`Proxy`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy) object has been updated to comply more with the ES6 specification: The [`defineProperty`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy/handler/defineProperty) and [`set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy/handler/set) handlers now need to explicitly return `true` to be successful, otherwise a [`TypeError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError) exception will be thrown in [strict mode](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode). Also, when the [`window`](https://developer.mozilla.org/en-US/docs/Web/API/Window) object is set as the target, those handlers will throw a `TypeError` starting with Firefox 39.
