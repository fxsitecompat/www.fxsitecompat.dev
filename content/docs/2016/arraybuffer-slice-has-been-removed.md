---
title: "`ArrayBuffer.slice()` has been removed"
date: "2016-12-04T19:50:00-05:00"
categories: ["javascript"]
tags: []
versions: ["53"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1313112"
      title: "Bug 1313112 - Deprecate and remove ArrayBuffer.slice"
aliases:
    - "/en-CA/docs/2016/arraybuffer-slice-will-be-removed/"
---
The non-standard `ArrayBuffer.slice` static method, [deprecated since Firefox 52](https://www.fxsitecompat.com/en-CA/docs/2016/arraybuffer-slice-has-been-deprecated/), has been removed with Firefox 53. Use the standard [`ArrayBuffer.prototype.slice`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer/slice) method instead.
