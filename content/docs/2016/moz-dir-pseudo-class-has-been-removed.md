---
title: "`:-moz-dir` pseudo-class has been removed"
date: "2016-11-25T18:48:00-05:00"
categories: ["css"]
tags: []
versions: ["53"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1270406"
      title: "Bug 1270406 - remove pseudo class :-moz-dir after :dir is shipped"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/F0_UbXAfB_4/discussion"
      title: "Intent to ship: unprefix :dir pseudo-class"
---
The prefixed `:-moz-dir` pseudo-class, deprecated since [Firefox 49](https://www.fxsitecompat.com/en-CA/docs/2016/dir-css-pseudo-class-has-been-unprefixed/), has been removed with Firefox 53. Use the standard, unprefixed [`:dir`](https://developer.mozilla.org/docs/Web/CSS/:dir) pseudo-class instead.
