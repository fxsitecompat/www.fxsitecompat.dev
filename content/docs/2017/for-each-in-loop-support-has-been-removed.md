---
title: "`for-each-in` loop support has been removed"
date: "2017-08-08T07:32:00-04:00"
categories: ["javascript"]
tags: []
releases: ["57", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1293205"
      title: "Bug 1293205 - Warn about non-standard for-each regardless of JS version number"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1293305"
      title: "Bug 1293305 - Disable non-standard for-each on nightly-only"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083470"
      title: "Bug 1083470 - Disable SpiderMonkey support for E4X for-each"
aliases:
    - "/en-CA/docs/2015/for-each-in-loop-support-will-be-removed/"
---
The support for the [`for each...in`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for_each...in) statement, [deprecated since Firefox 37](https://www.fxsitecompat.dev/en-CA/docs/2015/for-each-in-loops-are-now-deprecated/) has been removed with Firefox 57, because it's not a part of the ECMAScript 2015 (ES6) spec. It has already been disabled on the Nightly channel since Firefox 53. Use the standard [`for...of`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of) statement instead.
