---
title: "Expression closure support will be removed"
date: "2015-10-26T15:49:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083458"
      title: "Bug 1083458 - Remove SpiderMonkey support for expression closures (shorthand function syntax)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1319512"
      title: "Bug 1319512 - Disable non-standard expression closure on nightly-only"
---
The support for the non-standard [expression closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Expression_closures) (shorthand function syntax), [deprecated since Firefox 45](https://www.fxsitecompat.com/en-CA/docs/2015/expression-closures-are-now-deprecated/), will be removed in the future. Use the standard [arrow function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions) syntax instead.

**Update**: The expression closure support has been disabled on Firefox Nightly since Firefox 59.
