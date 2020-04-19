---
title: "`requiredFeatures` has been removed from some SVG interfaces"
date: "2019-07-07T01:48:00-04:00"
categories: ["svg"]
tags: []
releases: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1295404"
      title: "Bug 1295404 - remove requiredFeatures from SVGTests"
---
As of Firefox 69, the `requiredFeatures` property has been removed from the `SVGTests` mixin interface, which is implemented by some SVG interfaces including `SVGAnimationElement`, `SVGGraphicsElement` and `SVGImageElement`. The property was defined in the SVG 1.0 spec but later removed with SVG 2.0. It has already been removed with [Google Chrome 59](https://www.chromestatus.com/feature/5720709590417408).
