---
title: "Cross-frame `for-in` loop is not working"
date: "2015-10-22T22:58:00-07:00"
categories: ["javascript"]
tags: []
versions: ["37"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1152550"
      title: "Bug 1152550 - Cross-frame for-in is broken on Firefox 37, 38 beta"
---
Firefox 37 has a regression where the [`for...in`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in) statement doesn't work over cross-frame objects, throwing a `TypeError`. Some sites using *Google Caja* might be broken. This issue has been fixed with Firefox 38.
