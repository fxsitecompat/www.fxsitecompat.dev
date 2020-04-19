---
title: "`:dir` CSS pseudo-class has been unprefixed"
date: "2016-05-10T13:02:00-04:00"
categories: ["css"]
tags: []
versions: ["49", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=859301"
      title: "Bug 859301 - Unprefix css4 :dir"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1270406"
      title: "Bug 1270406 - remove pseudo class :-moz-dir after :dir is shipped"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/F0_UbXAfB_4/discussion"
      title: "Intent to ship: unprefix :dir pseudo-class"
---
The [`:dir`](https://developer.mozilla.org/docs/Web/CSS/:dir) CSS4 pseudo-class is now available in Firefox without the vender prefix. The prefixed `:-moz-dir` pseudo-class will be removed in the near future.
