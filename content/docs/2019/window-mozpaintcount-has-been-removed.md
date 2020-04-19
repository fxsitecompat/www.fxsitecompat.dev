---
title: "`window.mozPaintCount` has been removed"
date: "2019-10-29T07:50:00-04:00"
categories: ["dom"]
tags: []
releases: ["72"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1591968"
      title: "Bug 1591968 - Consider removing window.mozPaintCount."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/sZbx3Q2hIpA/discussion"
      title: "Intent to unship: window.mozPaintCount."
---
The non-standard [`window.mozPaintCount`](https://developer.mozilla.org/docs/Web/API/Window/mozPaintCount) property has been dropped with Firefox 72. Given that the API not implemented in any other browser, the compatibility risk should be very low unless it's used for a browser detection purpose.
