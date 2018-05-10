---
title: "`navigator.registerContentHandler()` has been removed"
date: "2018-05-09T22:43:00-04:00"
categories: ["dom"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1460481"
      title: "Bug 1460481 - Disable registerContentHandler() in stable"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/jeTDLz38_RE/discussion"
      title: "Intent to unship: navigator.registerContentHandler()"
---
The [`navigator.registerContentHandler`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/registerContentHandler) method, deprecated since [Firefox 59](https://www.fxsitecompat.com/en-CA/docs/2018/navigator-registercontenthandler-has-been-deprecated/), has been removed with Firefox 62. While it had been standardized in the HTML spec, no other browsers support the functionality and even the Firefox implementation wasn't aligned with the standard. Given the decreasing popularity of web feeds, the risk of the removal should be low.
