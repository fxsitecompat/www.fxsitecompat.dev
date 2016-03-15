---
title: "`getElementById` and several properties will be removed from `SVGSVGElement`"
date: "2015-10-28T01:11:00-07:00"
categories: ["svg"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1133173"
      title: "Bug 1133173 - remove SVGSVGElement.getElementById"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1174097"
      title: "Bug 1174097 - remove SVGSVGElement.useCurrentView"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1133175"
      title: "Bug 1133175 - remove SVGTests.hasExtension"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1133172"
      title: "Bug 1133172 - remove SVGSVGElement.{pixel,screenPixel}UnitToMillimeter{X,Y}"
---
The `getElementById` method as well as the `useCurrentView`, `pixelUnitToMillimeterX`, `pixelUnitToMillimeterY`, `screenPixelToMillimeterX` and `screenPixelToMillimeterY` properties will be removed from the [`SVGSVGElement`](https://developer.mozilla.org/en-US/docs/Web/API/SVGSVGElement) interface.

At the same time, the `hasExtension` method will be removed from the [`SVGTests`](https://developer.mozilla.org/en-US/docs/Web/API/SVGTests) interface, while the `nearestViewportElement` and `farthestViewportElement` properties will be removed from the `SVGGraphicsElement` interface.
