---
title: "`xml:base` attribute is no longer supported"
date: "2018-12-24T23:47:00-05:00"
categories: ["misc"]
tags: []
releases: ["66", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=903372"
      title: "Bug 903372 - Remove support for xml:base"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/goHxC7z3D7Q/discussion"
      title: "Intent to unship xml:base"
---
The support for the [`xml:base`](https://www.w3.org/TR/xmlbase/) attribute, deprecated since [Firefox 53](https://www.fxsitecompat.dev/en-CA/docs/2017/xml-base-attribute-has-been-deprecated/), has been removed with Firefox 66. The feature similar to the HTML [`<base>`](https://developer.mozilla.org/docs/Web/HTML/Element/base) element was removed from the spec years ago and no other browsers support it at this time, so the risk of the removal should be very low.
