---
title: "XHR `responseURL` no longer includes fragment"
date: "2014-10-17T22:50:44-04:00"
categories: ["dom"]
tags: []
versions: ["35"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1073882": "Bug 1073882 – XMLHttpRequest.prototype.responseURL should not have fragment per latest spec"
---
The [`XMLHttpRequest.responseURL`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest.responseURL) property now returns the URL of a response without the fragment beginning with a hash (`#`), according the latest [`XMLHttpRequest`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) spec.
