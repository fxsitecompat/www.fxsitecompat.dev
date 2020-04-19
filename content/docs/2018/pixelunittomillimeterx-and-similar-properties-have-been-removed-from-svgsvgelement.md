---
title: "`pixelUnitToMillimeterX` and similar properties have been removed from `SVGSVGElement`"
date: "2018-04-22T17:47:00-04:00"
categories: ["dom", "svg"]
tags: []
versions: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1133172"
      title: "Bug 1133172 - remove SVGSVGElement.{pixel,screenPixel}UnitToMillimeter{X,Y}"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/-Vhlz6uEVOA/discussion"
      title: " Intent to unship: SVGSVGElement.{pixel, screenPixel}UnitToMillimeter{X, Y} "
---
The `pixelUnitToMillimeterX`, `pixelUnitToMillimeterY`, `screenPixelToMillimeterX` and `screenPixelToMillimeterY` properties have been removed from the [`SVGSVGElement`](https://developer.mozilla.org/docs/Web/API/SVGSVGElement) interface. Those were defined in the SVG 1.1 spec but removed with SVG 2 due to lack of use. Given that [Google Chrome 47](https://www.chromestatus.com/feature/5478103916740608) shipped in December 2015 has already removed them, the compatibility risk should be very low.
