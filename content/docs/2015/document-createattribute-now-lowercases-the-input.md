---
title: "`document.createAttribute()` now lowercases the input"
date: "2015-12-16T10:27:00-05:00"
categories: ["dom"]
tags: []
releases: ["44", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1176313"
      title: "Bug 1176313 - Make Attr follow the spec again"
---
The implementation of the [`document.createAttribute`](https://developer.mozilla.org/docs/Web/API/Document/createAttribute) method has been updated for the latest DOM spec to make the given attribute name lowercase. According to Mozilla's investigation, less than 0.001% of Web pages may be affected by this change.
