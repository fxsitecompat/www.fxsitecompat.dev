---
title: "`DocumentType.internalSubset` has been removed"
date: "2015-10-20T15:37:00-07:00"
categories: ["dom"]
tags: []
versions: ["44"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=801545": "Bug 801545 - Remove obsolete attribute: DocumentType.internalSubset"
    "https://groups.google.com/d/topic/mozilla.dev.platform/u32smeY40Xw/discussion": "Intent to unship: DocumentType.internalSubset"
---
The obsolete, obscure `DocumentType.internalSubset` property, available on [`document.doctype`](https://developer.mozilla.org/en-US/docs/Web/API/Document/doctype), has been removed as it's gone from the DOM spec.
