---
title: "`navigator.registerContentHandler()` has been deprecated"
date: "2018-01-06T04:26:00-05:00"
categories: ["dom"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1398169"
      title: "Bug 1398169 - Remove registerContentHandler()"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/jeTDLz38_RE/discussion"
      title: "Intent to unship: navigator.registerContentHandler()"
---
The [`navigator.registerContentHandler`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/registerContentHandler) method, which could used to [bind feed reader services](https://developer.mozilla.org/en-US/Firefox/Releases/2/Adding_feed_readers_to_Firefox) to the browser, is now considered deprecated and will be removed in the near future. It's disabled by default in Nightly and early Beta/DevEdition as of Firefox 59. While it had been standardized in the HTML spec, no other browsers support the functionality and even the Firefox implementation wasn't aligned with the standard. Given the decreasing popularity of web feeds, the risk of the removal should be low.

**Update**: This method has been removed with [Firefox 62](https://www.fxsitecompat.com/en-CA/docs/2018/navigator-registercontenthandler-has-been-removed/). The first version of this note mentioned Firefox 59, but it was still available in the Release channel at that time.
