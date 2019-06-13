---
title: "`for-each-in` loops are now deprecated"
date: "2015-01-16T09:37:54-05:00"
categories: ["javascript"]
tags: []
versions: ["37"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083467"
      title: "Bug 1083467 – Add console warnings for E4X for-each"
---
The [`for each...in`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for_each...in) statement, introduced with JavaScript 1.6 as part of the [ECMAScript for XML (E4X)](https://developer.mozilla.org/docs/Archive/Web/E4X) support, is now considered deprecated and will be removed in the near future. Consider using the ECMAScript 6 [`for...of`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of) statement instead. Note that the E4X support itself has already been [removed with Firefox 21](https://www.fxsitecompat.dev/en-CA/docs/2013/e4x-support-has-been-completely-removed/) and this statement has been kept just for backward compatibility.

**Update**: The support for the statement has been [removed with Firefox 57](https://www.fxsitecompat.dev/en-CA/docs/2017/for-each-in-loop-support-has-been-removed/).
