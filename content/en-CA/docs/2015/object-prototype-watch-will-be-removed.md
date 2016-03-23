---
title: "`Object.prototype.watch` will be removed"
date: "2015-10-26T15:35:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=638054"
      title: "Bug 638054 - JavaScript Object.prototype.watch should be removed, once an adequate debugger-only replacement exists"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=934669"
      title: "Bug 934669 - Deprecate Object.prototype.{,un}watch, and make them warn when used"
---
The non-standard [`Object.prototype.watch`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/watch) and [`Object.prototype.unwatch`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/unwatch) methods will be removed in the future. Use the standard [`Proxy`] (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy) object instead.
