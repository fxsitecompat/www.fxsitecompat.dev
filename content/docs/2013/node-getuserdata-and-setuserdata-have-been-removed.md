---
title: "`Node.getUserData()` and `setUserData()` have been removed"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
versions: ["22"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=842372"
      title: "Bug 842372 – Make getUserData and setUserData ChromeOnly"
---
The [`Node.getUserData`](https://developer.mozilla.org/docs/Web/API/Node.getUserData) and [`Node.setUserData`](https://developer.mozilla.org/docs/Web/API/Node.setUserData) methods are no longer available from Web contents. [`Element.dataset`](https://developer.mozilla.org/docs/Web/API/Element.dataset) or [`WeakMap`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) can be used instead.
