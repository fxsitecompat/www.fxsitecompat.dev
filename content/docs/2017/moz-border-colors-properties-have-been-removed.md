---
title: "`-moz-border-*-colors` properties have been removed"
date: "2017-12-06T11:20:00-05:00"
categories: ["css"]
tags: []
releases: ["59", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1417200"
      title: "Bug 1417200 - Make -moz-border-*-colors chrome only"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/D23VvCJO53Q/discussion"
      title: "Intent to unship -moz-border-*-colors from content pages."
---
Starting with Firefox 59, the following non-standard border colour properties are no longer available from web content:

* [`-moz-border-top-colors`](https://developer.mozilla.org/docs/Web/CSS/-moz-border-top-colors)
* [`-moz-border-right-colors`](https://developer.mozilla.org/docs/Web/CSS/-moz-border-right-colors)
* [`-moz-border-bottom-colors`](https://developer.mozilla.org/docs/Web/CSS/-moz-border-bottom-colors)
* [`-moz-border-left-colors`](https://developer.mozilla.org/docs/Web/CSS/-moz-border-left-colors)

Since those are not supported by any other browsers, the compatibility risk should be very low. Though there is no exact standard equivalent, the [`border-image`](https://developer.mozilla.org/docs/Web/CSS/border-image) property can be used to achieve gradient borders if needed.
