---
title: "`ArrayBuffer.slice()` has been deprecated"
date: "2016-11-16T19:34:00-05:00"
categories: ["javascript"]
tags: []
versions: ["52"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1316913"
      title: "Bug 1316913 - Warn about ArrayBuffer.slice"
---
The non-standard `ArrayBuffer.slice` static method has been deprecated and will be [removed from Firefox 53](https://www.fxsitecompat.dev/en-CA/docs/2016/arraybuffer-slice-will-be-removed/). Use the standard [`ArrayBuffer.prototype.slice`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer/slice) method instead.
