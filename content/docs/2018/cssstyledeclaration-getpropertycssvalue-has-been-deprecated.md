---
title: "`CSSStyleDeclaration.getPropertyCSSValue()` has been deprecated"
date: "2018-03-16T18:09:00-04:00"
categories: ["css", "dom"]
tags: []
releases: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=474655"
      title: "Bug 474655 - warn when nsIDOMCSSStyleDeclaration::GetPropertyCSSValue is called"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1448415"
      title: "Bug 1448415 - Hide getPropertyCSSValue on Nightly."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1461092"
      title: "Bug 1461092 - Unship GetPropertyCSSValue in beta."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/qu5JekiuSfw/discussion"
      title: "Intent to unship: CSSStyleDeclaration.getPropertyCSSValue"
---
The support for the [`getPropertyCSSValue`](https://developer.mozilla.org/docs/Web/API/CSSStyleDeclaration/getPropertyCSSValue) method on the `CSSStyleDeclaration` interface is now considered deprecated and will be removed in the near future. Firefox 61 and later will show a console warning for the method that has been [classified as obsolete](https://lists.w3.org/Archives/Public/www-style/2003Oct/0347.html) since 2003. Google Chrome has already [removed the support](https://groups.google.com/a/chromium.org/d/topic/blink-dev/3VmxWFzcyJc/discussion) back in 2014. Use the [`getPropertyValue`](https://developer.mozilla.org/docs/Web/API/CSSStyleDeclaration/getPropertyValue) method instead.

**Update**: The method has been disabled on the Nightly channel as of Firefox 61.

**Update 2**: The method has been disabled also on Firefox Beta and Developer Edition as of Firefox 61.

**Update 3**: The method has been [completely removed with Firefox 62](https://www.fxsitecompat.dev/en-CA/docs/2018/cssstyledeclaration-getpropertycssvalue-has-been-removed/).
