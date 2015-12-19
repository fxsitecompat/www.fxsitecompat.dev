---
title: "`RegExp.multiline` global switch will be removed"
date: "2015-12-19T01:10:00-05:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1219757": "Bug 1219757 - Remove nonstandard RegExp.multiline global switch"
---
The non-standard `multiline` property on the [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp) object, [deprecated since Firefox 46](https://www.fxsitecompat.com/en-US/docs/2015/regexp-multiline-global-switch-has-been-deprecated/), will be removed in the near future. Use the `m` flag for the `RegExp` literal and constructor instead. Note that the standard [`multiline`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/multiline) property on `RegExp` instances won't be removed.
