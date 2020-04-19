---
title: "`CSSStyleDeclaration.getPropertyCSSValue()` and related interfaces have been removed"
date: "2018-05-08T16:01:00-04:00"
categories: ["css", "dom"]
tags: []
releases: ["62", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1408301"
      title: "Bug 1408301 - unship CSSStyleDeclaration::getPropertyCSSValue"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1459871"
      title: "Bug 1459871 - Remove other getPropertyCssValue-related interfaces."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/qu5JekiuSfw/discussion"
      title: "Intent to unship: CSSStyleDeclaration.getPropertyCSSValue"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/3BAUfGbtWC4/discussion"
      title: "Intent to unship: getPropertyCSSValue-related interfaces Rect, RGBColor, CSSValue, CSSPrimitiveValue and CSSValueList"
aliases:
    - "/en-CA/docs/2018/cssstyledeclaration-getpropertycssvalue-has-been-removed/"
---
The support for the obsolete [`getPropertyCSSValue`](https://developer.mozilla.org/docs/Web/API/CSSStyleDeclaration/getPropertyCSSValue) method on the `CSSStyleDeclaration` interface, deprecated in [Firefox 61](https://www.fxsitecompat.dev/en-CA/docs/2018/cssstyledeclaration-getpropertycssvalue-has-been-deprecated/), has been removed with Firefox 62. The standard [`getPropertyValue`](https://developer.mozilla.org/docs/Web/API/CSSStyleDeclaration/getPropertyValue) method should be used instead. Given that Google Chrome has already [removed the support](https://groups.google.com/a/chromium.org/d/topic/blink-dev/3VmxWFzcyJc/discussion) back in 2014, the compatibility risk should be very low at this time.

**Update**: The following related interfaces have also been removed: [`CSSPrimitiveValue`](https://developer.mozilla.org/docs/Web/API/CSSPrimitiveValue), [`CSSValue`](https://developer.mozilla.org/docs/Web/API/CSSValue), [`CSSValueList`](https://developer.mozilla.org/docs/Web/API/CSSValueList), `Rect` and `RGBColor`.
