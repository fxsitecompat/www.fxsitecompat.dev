---
title: "`LSProgressEvent` has been removed"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
versions: ["22", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=845631"
      title: "Bug 845631 – Remove nsXMLHttpProgressEvent"
---
[`LSProgressEvent`](https://www.w3.org/TR/DOM-Level-3-LS/load-save.html#LS-LSProgressEvent), an old interface which has been used especially with [`XMLHttpRequest`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest) and [deprecated](https://bugzilla.mozilla.org/show_bug.cgi?id=616672) since Firefox 10, has been removed along with the `input`, `position`, `totalSize` attributes. As explained in the [Monitoring progress](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/Using_XMLHttpRequest#Monitoring_progress) section, the generic [`ProgressEvent`](https://developer.mozilla.org/docs/Web/API/ProgressEvent) interface can be used instead, including the `loaded` and `total` attributes.
