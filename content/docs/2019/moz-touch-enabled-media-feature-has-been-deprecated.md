---
title: "`-moz-touch-enabled` media feature has been deprecated"
date: "2019-10-20T13:19:00-04:00"
categories: ["css"]
tags: []
versions: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1035774"
      title: "Bug 1035774 - Implement Interaction Media Features including pointer:coarse that replaces non-standard -moz-touch-enabled"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1588737"
      title: "Bug 1588737 - The user is unable to scroll on feedmusic.com on Yoga devices (caused by Modernizr.touch having different values in Firefox vs. Chrome, caused by -moz-touch-enabled)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/SPmSiWfn1Ts/discussion"
      title: "Intent to unship: @media (-moz-touch-enabled)"
---
The [`-moz-touch-enabled`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-touch-enabled) CSS media feature is now disabled in the Nightly channel as of Firefox 71, and will be removed from all channels in the near future. The standard [Interaction Media Features](https://drafts.csswg.org/mediaqueries-4/#mf-interaction) have been supported since Firefox 64, and at least 1 site is known to be not scrollable in Firefox because of the *Modernizr* library's wrong detection using the non-standard media feature, hence the deprecation.

You can now use the [`pointer`](https://developer.mozilla.org/docs/Web/CSS/@media/pointer) media feature instead. For example, if you have `-moz-touch-enabled:1` in your media query, simply replace it with `pointer:coarse`.

This is the last remaining non-standard system metric media feature in Firefox. Others had already been removed with [Firefox 58](https://www.fxsitecompat.dev/en-CA/docs/2017/non-standard-system-metric-pseudo-classes-and-media-features-have-been-removed/).
