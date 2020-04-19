---
title: "`Node.attributes` has been removed"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
releases: ["22", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=844134"
      title: "Bug 844134 – attributes should be defined on Element and not Node"
---
The [`Node.attributes`](https://developer.mozilla.org/docs/Web/API/Node.attributes) property is no longer available, due to the removal from the spec. The [`Element.attributes`](https://developer.mozilla.org/docs/Web/API/Element.attributes) property is still available.
