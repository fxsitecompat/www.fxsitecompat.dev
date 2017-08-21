---
title: "`Object.prototype.watch` has been deprecated"
date: "2017-08-21T16:27:00-04:00"
categories: ["javascript"]
tags: []
versions: ["57"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=638054"
      title: "Bug 638054 - JavaScript Object.prototype.watch should be removed, once an adequate debugger-only replacement exists"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=934669"
      title: "Bug 934669 - Deprecate Object.prototype.{,un}watch, and make them warn when used"
aliases:
    - "/en-CA/docs/2015/object-prototype-watch-will-be-removed/"
    - "/en-CA/docs/2017/object-prototype-watch-will-be-removed/"
---
The non-standard [`Object.prototype.watch`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/watch) and [`unwatch`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/unwatch) methods are now considered deprecated and will be removed in the near future. Firefox 57 and later shows a warning in the Console for these methods. Use the standard [`Proxy`] (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy) or [`Reflect`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Reflect) object instead.
