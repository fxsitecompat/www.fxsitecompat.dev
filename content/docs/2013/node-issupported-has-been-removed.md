---
title: "`Node.isSupported()` has been removed"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
versions: ["22", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=801562"
      title: "Bug 801562 – Remove Node.isSupported"
---
The [`Node.isSupported`](https://developer.mozilla.org/docs/Web/API/Node.isSupported) method is no longer available, due to the removal from the spec. Since [Firefox 19](https://www.fxsitecompat.dev/en-CA/docs/2012/hasfeature-issupported-methods-now-always-return-true/), this method has always returned `true`.
