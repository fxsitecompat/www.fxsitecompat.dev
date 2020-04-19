---
title: "`MediaStream.currentTime` has been removed"
date: "2018-11-06T12:06:00-05:00"
categories: ["audio-video", "dom"]
tags: []
releases: ["65", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1502927"
      title: "Bug 1502927 - Remove MediaStream.currentTime"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/QW7_dfNSWLw/discussion"
      title: "Intent to unship: MediaStream.currentTime"
---
Firefox 65 has removed the non-standard `currentTime` property from the `MediaStream` interface. It has never been standardized in the spec and never been implemented by other browsers, so the risk of the removal should be very low.
