---
title: "`XMLHttpRequest.sendAsBinary` has been deprecated"
date: "2014-04-03T19:31:02-04:00"
categories: ["dom"]
tags: []
versions: ["31"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=939323": "Bug 939323 – Warn about XMLHttpRequest sendAsBinary usage"
---
The non-standard `sendAsBinary` method on the [`XMLHttpRequest`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) interface is now considered deprecated and will be removed soon. The standard `send(Blob)` method can be used instead.

**Update**: This method has been [removed with Firefox 39](https://www.fxsitecompat.com/en-CA/docs/2015/xmlhttprequest-sendasbinary-has-been-removed/).
