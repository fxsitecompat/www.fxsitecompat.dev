---
title: "`document.createAttribute` now lowercases the input"
date: "2015-12-16T10:27:00-05:00"
categories: ["dom"]
tags: []
versions: ["44"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1176313": "Bug 1176313 - Make Attr follow the spec again"
---
The implementation of the [`document.createAttribute`](https://developer.mozilla.org/en-US/docs/Web/API/Document/createAttribute) method has been updated for the latest DOM spec to make the given attribute name lowercase. According to Mozilla's investigation, less than 0.001% of Web pages may be affected by this change.
