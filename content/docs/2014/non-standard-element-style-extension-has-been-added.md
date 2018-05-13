---
title: "Non-standard `element.style` extension has been added"
date: "2014-10-17T22:50:44-04:00"
categories: ["dom"]
tags: []
versions: ["35"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=958887"
      title: "Bug 958887 – Add support for element.style[\"css-property-name\"] non-standard extension"
---
Firefox now supports the [`HTMLElement.style`](https://developer.mozilla.org/docs/Web/API/HTMLElement.style) property's non-standard extension that allows developers to get and set a CSS property using a simple syntax like `element.style["css-property-name"]`. This improves interoperability since all other major browsers support it.
