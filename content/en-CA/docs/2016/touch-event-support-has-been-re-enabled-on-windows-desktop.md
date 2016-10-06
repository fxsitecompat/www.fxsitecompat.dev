---
title: "Touch event support has been re-enabled on Windows desktop"
date: "2016-10-06T08:23:00-04:00"
categories: ["dom"]
tags: []
versions: ["52"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=806805"
      title: "Bug 806805 - [meta] Mouse / touch input problems on Windows devices that support touch input"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1180706"
      title: "Bug 1180706 - [meta] Touch support in APZ on desktop platforms"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1244402"
      title: "Bug 1244402 - Let touch events on windows ride the trains"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/4pPJfp_aSKE/discussion"
      title: "Touch events enabled on Windows desktop (nightly only)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6CGjsm1XpD4/discussion"
      title: "Intent to ship: TouchEvents (Windows), touch-action (all platforms), accessible caret"
---
The support for the standard [touch events](https://developer.mozilla.org/en-US/docs/Web/API/Touch_events) on Windows desktop platforms, [introduced with Firefox 18](https://www.fxsitecompat.com/en-CA/docs/2012/moztouch-events-were-removed-in-favour-of-the-standard-touch-events/) but [disabled with Firefox 24](https://www.fxsitecompat.com/en-CA/docs/2013/touch-events-support-has-been-temporarily-disabled-on-desktop/) due to various site compatibility issues, is now enabled again with Firefox 52. On Firefox Nightly, this has already been enabled since Firefox 47.

While most of the bugs have been solved by Firefox or the sites in question, there may still be some more unreported issues. Basically, Web developers should never rely on touch events to detect if the user is on mobile, otherwise your site may cause unexpected UX issues on desktop and laptop computers with a touch screen. 

For a quick test, you can use the [Responsive Design Mode](https://developer.mozilla.org/en-US/docs/Tools/Responsive_Design_Mode) in Firefox Developer Tools to simulate touch events.
