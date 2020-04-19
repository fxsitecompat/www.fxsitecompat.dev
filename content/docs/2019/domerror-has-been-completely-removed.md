---
title: "`DOMError` has been completely removed"
date: "2019-06-17T18:30:00-04:00"
categories: ["dom"]
tags: []
releases: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1558387"
      title: "Bug 1558387 - Remove DOMError constructor"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6yQtQoNeR-s/discussion"
      title: "Intent to unship: DOMError"
---
Firefox 69 has removed the now-non-standard `DOMError` interface, which had been deprecated since [Firefox 58](https://www.fxsitecompat.dev/en-CA/docs/2017/domerror-has-been-replaced-with-domexception/) when all the instances were replaced with `DOMException`. The current usage is nearly zero according to Mozilla's Telemetry, so the compatibility risk of the removal should be low.
