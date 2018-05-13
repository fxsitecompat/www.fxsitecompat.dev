---
title: "`CSSStyleDeclaration.getPropertyCSSValue()` has been removed"
date: "2018-05-08T16:01:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1408301"
      title: "Bug 1408301 - unship CSSStyleDeclaration::getPropertyCSSValue"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/qu5JekiuSfw/discussion"
      title: "Intent to unship: CSSStyleDeclaration.getPropertyCSSValue"
---
The support for the obsolete [`getPropertyCSSValue`](https://developer.mozilla.org/docs/Web/API/CSSStyleDeclaration/getPropertyCSSValue) method on the `CSSStyleDeclaration` interface, deprecated in [Firefox 61](https://www.fxsitecompat.com/en-CA/docs/2018/cssstyledeclaration-getpropertycssvalue-has-been-deprecated/), has been removed with Firefox 62. The standard [`getPropertyValue`](https://developer.mozilla.org/docs/Web/API/CSSStyleDeclaration/getPropertyValue) method should be used instead. Given that Google Chrome has already [removed the support](https://groups.google.com/a/chromium.org/d/topic/blink-dev/3VmxWFzcyJc/discussion) back in 2014, the compatibility risk should be very low at this time.
