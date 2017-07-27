---
title: "`XMLHttpRequest.sendAsBinary` has been removed"
date: "2015-03-17T14:02:59-04:00"
categories: ["dom"]
tags: []
versions: ["39"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=853162"
      title: "Bug 853162 - Remove XMLHttpRequest sendAsBinary"
---
The non-standard [`XMLHttpRequest.prototype.sendAsBinary`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest#sendAsBinary) method, [deprecated since Firefox 31](https://www.fxsitecompat.com/en-CA/docs/2014/xmlhttprequest-sendasbinary-has-been-deprecated/), has been removed. The standard `send(Blob)` method should be used instead.
