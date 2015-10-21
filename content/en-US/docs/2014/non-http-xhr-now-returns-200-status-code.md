---
title: "Non-HTTP XHR now returns `200` status code"
date: "2014-10-17T22:50:44-04:00"
categories: ["dom"]
tags: []
versions: ["35"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=716491": "Bug 716491 – Investigate the status code for non-HTTP XHR."
---
The status code for successful non-HTTP [`XMLHttpRequest`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) responses has been changed from `0` to `200` to follow the spec.
