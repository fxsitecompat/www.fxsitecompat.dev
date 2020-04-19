---
title: "CSS radial gradients no longer accept negative radii"
date: "2019-10-02T17:07:00-04:00"
categories: ["css"]
tags: []
releases: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1583736"
      title: "Bug 1583736 - CSS radial-gradient should not accept negative radii"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vCIpV5oCAtg/discussion"
      title: "Intent to unship: Negative radii in radial gradients."
---
Starting with Firefox 71, both the prefixed and unprefixed [`radial-gradient()`](https://developer.mozilla.org/docs/Web/CSS/radial-gradient) CSS functions will ignore parameters with any negative length, which has been invalid in the spec but supported in all browsers. The following declarations, for example, won't work any more:

```css
background-image: radial-gradient(-100px 25px, red, green);
background-image: -moz-radial-gradient(50%, -100px -10%, red, blue);
background-image: -webkit-gradient(radial, 1 2, -1.5, 50% 50%, 10000);
```

[Google Chrome](https://bugs.chromium.org/p/chromium/issues/detail?id=1008112) has made the same change in the recent version, and [Safari](https://bugs.webkit.org/show_bug.cgi?id=202412) may also follow.
