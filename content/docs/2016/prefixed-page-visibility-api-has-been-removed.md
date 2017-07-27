---
title: "Prefixed Page Visibility API has been removed"
date: "2016-09-07T18:11:00-04:00"
categories: ["dom"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=812701"
      title: "Bug 812701 - Drop the prefixed version of visibility API"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/FkAJkVOJF74/discussion"
      title: "Intent to unship: -moz-prefixed Page Visibility API."
aliases:
    - "/en-CA/docs/2015/prefixed-page-visibility-api-will-be-removed/"
    - "/en-CA/docs/2016/prefixed-page-visibility-api-has-been-be-removed/"
---
The support for the prefixed [Page Visibility API](https://developer.mozilla.org/en-US/docs/Web/API/Page_Visibility_API), [deprecated since Firefox 18](https://www.fxsitecompat.com/en-CA/docs/2012/page-visibility-api-has-been-unprefixed/), has been removed with Firefox 51. This includes the `mozHidden` and `mozVisibilityState` properties as well as the `mozvisibilitychange` event. Use the unprefixed, standard equivalents instead.
