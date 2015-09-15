---
title: "XBL-related methods have been removed"
date: "2013-09-19T23:58:13-04:00"
categories: ["dom"]
tags: []
versions: "26"
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=912322": "Bug 912322 – document.getAnonymous* should not be available to web content"
---
The following methods implemented on the [XBL DOM interface](https://developer.mozilla.org/en-US/docs/XBL/XBL_1.0_Reference/DOM_Interfaces) have been removed from the [`Document`](https://developer.mozilla.org/en-US/docs/Web/API/Document) interface: `getAnonymousNodes`, `getAnonymousElementByAttribute`, `getBindingParent`, and `loadBindingDocument`.
