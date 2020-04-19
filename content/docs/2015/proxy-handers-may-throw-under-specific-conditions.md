---
title: "`Proxy` handers may throw under specific conditions"
date: "2015-03-17T14:02:59-04:00"
categories: ["javascript"]
tags: []
versions: ["39", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1132522"
      title: "Bug 1132522 - Treat false return value from certain Proxy handler methods as failure"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=828137"
      title: "Bug 828137 - Need APIs that would allow proxies to implement Reject in spec terms"
---
The implementation of the [`Proxy`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy) object has been updated to comply more with the ES6 specification: The [`defineProperty`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy/handler/defineProperty) and [`set`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy/handler/set) handlers now need to explicitly return `true` to be successful, otherwise a [`TypeError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/TypeError) exception will be thrown in [strict mode](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Strict_mode). Also, when the [`window`](https://developer.mozilla.org/docs/Web/API/Window) object is set as the target, those handlers will throw a `TypeError` starting with Firefox 39.
