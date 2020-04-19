---
title: "`SVGDocument` has been removed"
date: "2016-10-05T07:06:00-04:00"
categories: ["dom", "svg"]
tags: []
versions: ["52", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1293786"
      title: "Bug 1293786 - Remove SVGDocument"
---
The `SVGDocument` interface has been removed since it no longer exists in the SVG 2 spec. The SVG document type will be [`XMLDocument`](https://developer.mozilla.org/docs/Web/API/XMLDocument) instead. The `rootElement` property has been moved to the [`Document`](https://developer.mozilla.org/docs/Web/API/Document) interface so it's still available.
