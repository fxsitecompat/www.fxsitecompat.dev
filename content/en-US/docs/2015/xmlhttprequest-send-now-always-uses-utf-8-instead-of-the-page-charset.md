---
title: "`XMLHttpRequest.send` now always uses UTF-8 instead of the page charset"
date: "2015-01-16T09:37:54-05:00"
categories: ["dom"]
tags: []
versions: "37"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1109486": "Bug 1109486 – XMLHttpRequest.send(document) should unconditionally encode as UTF-8"
---
The implementation of the [`XMLHttpRequest.send()`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest#send%28%29) method has been updated so it will always send the passed data as `UTF-8` instead of the document's character encoding, as per the spec.
