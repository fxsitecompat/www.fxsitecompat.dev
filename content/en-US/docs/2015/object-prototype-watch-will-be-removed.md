---
title: "`Object.prototype.watch` will be removed"
date: "2015-10-26T15:35:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=934669": "Bug 934669 - Deprecate Object.prototype.{,un}watch, and make them warn when used"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=800355": "Bug 800355 - Implement Object.observe"
---
The non-standard [`Object.prototype.watch`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/watch) and [`Object.prototype.unwatch`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/unwatch) methods will be removed in the future. The [`Proxy`] (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy) object and the [`Object.observe`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/observe) method are the standard alternatives, though the latter is not implemented in Firefox yet.
