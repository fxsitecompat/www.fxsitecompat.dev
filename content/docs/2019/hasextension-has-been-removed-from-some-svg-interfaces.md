---
title: "`hasExtension()` has been removed from some SVG interfaces"
date: "2019-05-27T23:39:00-04:00"
categories: ["svg"]
tags: []
versions: ["68"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1133175"
      title: "Bug 1133175 - remove SVGTests.hasExtension"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/WLNCdEM1x44/discussion"
      title: "Intent to unship: hasFeature() method on some SVG elements"
---
As of Firefox 68, the `hasExtension` method has been removed from the `SVGTests` mixin interface, which is implemented by some SVG interfaces including `SVGAnimationElement`, `SVGGraphicsElement` and `SVGImageElement`. The method was defined in the SVG 1.0 spec but later removed with SVG 2.0. It has already been removed with [Google Chrome 47](https://www.chromestatus.com/feature/5473526421127168).
