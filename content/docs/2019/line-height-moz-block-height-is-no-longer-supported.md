---
title: "`line-height:-moz-block-height` is no longer supported"
date: "2019-05-28T04:06:00-04:00"
categories: ["css"]
tags: []
releases: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1540093"
      title: "Bug 1540093 - Unship line-height: -moz-block-height."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/XA2mqBeNrk4/discussion"
      title: "Intent to Unship: -moz-block-height value for line-height"
---
The non-standard `-moz-block-height` value for the CSS `line-height` property, which makes the line height the height of the containing block, is no longer available from web content. It's supposed to be for Firefox's internal use only. Given that it's implemented in no other browsers, the compatibility risk should be very low.
