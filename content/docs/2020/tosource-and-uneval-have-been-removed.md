---
title: "`toSource()` and `uneval()` have been removed"
date: "2020-01-11T01:37:00-05:00"
categories: ["javascript"]
tags: []
versions: ["74"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1565170"
      title: "Bug 1565170 - Disable toSource/uneval in non-chrome code"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/WVk3jvpzsgs/discussion"
      title: "Intent to unship: JavaScript toSource and uneval"
---
Firefox 74 has removed the non-standard [`Object.prototype.toSource`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/toSource) method, which was inherited by every object derived from `Object` including `Array`, `Date` and `Function`, as well as the [`uneval`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/uneval) global function. Unlike the standard `toString` method and the `eval` global function, no other browsers support those Netscape legacies, so the compatibility risk should be low.
