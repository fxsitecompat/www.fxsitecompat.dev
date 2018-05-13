---
title: "`Node.hasAttributes` has been moved to `Element`"
date: "2014-10-17T22:50:44-04:00"
categories: ["dom"]
tags: []
versions: ["35"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1055773"
      title: "Bug 1055773 – Move hasAttributes() to Element"
---
The deprecated `hasAttributes` method has been removed from the [`Node`](https://developer.mozilla.org/docs/Web/API/Node) interface. This change should not affect general use cases because the [`Element.hasAttributes`](https://developer.mozilla.org/docs/Web/API/Element.hasAttributes) method does the same thing.
