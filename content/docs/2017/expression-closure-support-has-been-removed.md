---
title: "Expression closure support has been removed"
date: "2017-12-26T10:51:00-05:00"
categories: ["javascript"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083458"
      title: "Bug 1083458 - Remove SpiderMonkey support for expression closures (shorthand function syntax)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1319512"
      title: "Bug 1319512 - Disable non-standard expression closure on nightly-only"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1426519"
      title: "Bug 1426519 - Disable non-standard expression closure everywhere"
aliases:
    - "/en-CA/docs/2015/expression-closure-support-will-be-removed/"
---
The support for the non-standard [expression closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Expression_closures) (shorthand function syntax), [deprecated since Firefox 45](https://www.fxsitecompat.com/en-CA/docs/2015/expression-closures-are-now-deprecated/), has been removed with Firefox 59. Use the standard [arrow function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions) syntax instead.
