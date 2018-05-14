---
title: "`let` expression support has been dropped"
date: "2015-06-13T15:20:46-04:00"
categories: ["javascript"]
tags: []
versions: ["41"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1023609"
      title: "Bug 1023609 - Remove SpiderMonkey support for let expressions"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1167029"
      title: "Bug 1167029 - Remove SpiderMonkey support for let blocks"
---
The support for the non-standard [`let` expressions](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/let#let_expressions), introduced with [JavaScript 1.7](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.7) and [deprecated since Firefox 36](https://www.fxsitecompat.com/en-CA/docs/2014/let-blocks-and-expressions-have-been-deprecated/), has been removed to comply with the ECMAScript 6 specification. The [`let` block](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/let#let_blocks) support will also be removed soon.
