---
title: "`hasFeature()` will always return `true` even for SVG"
date: "2016-09-06T22:24:00-04:00"
categories: ["dom", "svg"]
tags: []
releases: ["51", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=984778"
      title: "Bug 984778 - Make hasFeature() always return true (even for SVG)"
---
Since [Firefox 19](https://www.fxsitecompat.dev/en-CA/docs/2012/hasfeature-issupported-methods-now-always-return-true/), the [`document.implementation.hasFeature`](https://developer.mozilla.org/docs/Web/API/DOMImplementation/hasFeature) method is returning `true` except for SVG features. Firefox 51 has removed this exception so that it will ignore the parameters and always return `true` from now on. Given that Google Chrome is already returning `true` since the version 44 released in July 2015, the compatibility impact should be minimum.
