---
title: "`SVGZoomEvent` has been removed"
date: "2017-04-05T16:56:00-04:00"
categories: ["dom", "svg"]
tags: []
releases: ["55", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1314388"
      title: "Bug 1314388 - Remove SVGZoomEvent"
---
The support for the [`SVGZoomEvent`](https://www.w3.org/TR/SVG/script.html#InterfaceSVGZoomEvent) interface and event, its variant `SVGZoomEvents`, and the `onzoom` attribute for the `<svg>` root element has been removed with Firefox 55 since these are no longer included in the SVG 2 spec.
