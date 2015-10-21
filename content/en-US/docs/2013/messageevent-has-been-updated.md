---
title: "`MessageEvent` has been updated"
date: "2013-09-19T23:58:13-04:00"
categories: ["dom"]
tags: []
versions: ["26"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=848294": "Bug 848294 – Update MessageEvent to be compatible with the spec"
---
The [`MessageEvent`](https://developer.mozilla.org/en-US/docs/Web/API/MessageEvent) interface has been updated to comply with the latest spec. The `initMessageEvent` method has been removed while the interface is now a constructor.

**Update**: The `initMessageEvent` method has been [re-added to Firefox 44](https://bugzilla.mozilla.org/show_bug.cgi?id=949376) because it's back to the spec.
