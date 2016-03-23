---
title: "`RegExp.multiline` global switch has been removed"
date: "2016-03-23T05:30:00-04:00"
categories: ["javascript"]
tags: []
versions: ["48"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1219757"
      title: "Bug 1219757 - Remove nonstandard RegExp.multiline global switch"
aliases:
    - "/docs/2015/regexp-multiline-global-switch-will-be-removed/"
---
The non-standard `multiline` property on the [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp) object, [deprecated since Firefox 46](https://www.fxsitecompat.com/en-CA/docs/2015/regexp-multiline-global-switch-has-been-deprecated/), has been removed with Firefox 48. Use the `m` flag for the `RegExp` literal and constructor instead. Note that the standard [`multiline`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/multiline) property on `RegExp` instances won't be removed.
