---
title: "`let` block support has been removed"
date: "2015-10-24T22:00:00-07:00"
categories: ["javascript"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1167029"
      title: "Bug 1167029 - Remove SpiderMonkey support for let blocks"
aliases:
    - "/en-CA/docs/2015/let-block-support-will-be-dropped/"
---
The support for the non-standard [`let` blocks](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/let#let_blocks), introduced with [JavaScript 1.7](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.7) and [deprecated since Firefox 36](https://www.fxsitecompat.dev/en-CA/docs/2014/let-blocks-and-expressions-have-been-deprecated/), has been removed with Firefox 44, to comply with the ECMAScript 2015 (ES6) spec. The [`let` expression](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/let#let_expressions) support has already been [removed with Firefox 41](https://www.fxsitecompat.dev/en-CA/docs/2015/let-expression-support-has-been-dropped/).
