---
title: "`image-orientation` property no longer accepts angle values"
date: "2018-08-14T23:13:00-04:00"
categories: ["css"]
tags: []
versions: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1473450"
      title: "Bug 1473450 - remove <angle> values from image-orientation"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/A1aaENcsR6k/discussion"
      title: "Intent to unship: explicit <angle> values in image-orientation"
---
Firefox 63 has dropped the support for explicit angle values and the `flip` keyword for the CSS [`image-orientation`](https://developer.mozilla.org/docs/Web/CSS/image-orientation) property, according to the latest CSS Images Module spec. The initial value will be `none` instead of `0deg`, and `from-image` will be the only keyword you can use. Given that the property has been implemented only in Firefox so far, the compatibility risk should be very low.
