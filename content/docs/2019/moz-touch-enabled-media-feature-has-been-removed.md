---
title: "`-moz-touch-enabled` media feature has been removed"
date: "2019-12-07T17:00:00-05:00"
categories: ["css"]
tags: []
versions: ["73"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1486964"
      title: "Bug 1486964 - Drop -moz-touch-enabled"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/SPmSiWfn1Ts/discussion"
      title: "Intent to unship: @media (-moz-touch-enabled)"
---
The [`-moz-touch-enabled`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-touch-enabled) CSS media feature, deprecated since [Firefox 71](https://www.fxsitecompat.dev/en-CA/docs/2019/moz-touch-enabled-media-feature-has-been-deprecated/), has been removed from all channels with Firefox 73. The standard [Interaction Media Features](https://drafts.csswg.org/mediaqueries-4/#mf-interaction) have been supported since Firefox 64, and at least 1 site was known to be not scrollable in Firefox because of the *Modernizr* library's wrong detection using the non-standard media feature.

You can now use the [`pointer`](https://developer.mozilla.org/docs/Web/CSS/@media/pointer) media feature instead. For example, if you have `-moz-touch-enabled:1` in your media query, simply replace it with `pointer:coarse`.

This was the last remaining non-standard system metric media feature in Firefox. Others had already been removed with [Firefox 58](https://www.fxsitecompat.dev/en-CA/docs/2017/non-standard-system-metric-pseudo-classes-and-media-features-have-been-removed/).
