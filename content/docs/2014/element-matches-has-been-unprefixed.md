---
title: "`Element.matches()` has been unprefixed"
date: "2014-09-01T22:12:15-04:00"
categories: ["dom"]
tags: []
versions: ["34", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=886308"
      title: "Bug 886308 – Implement Element.matches()"
---
The [`Element.matches`](https://developer.mozilla.org/docs/Web/API/Element.matches) method has finally been unprefixed since the spec is now considered stable. The prefixed `mozMatchesSelector` method will be removed in the future.
