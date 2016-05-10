---
title: "`:dir` CSS pseudo-class has been unprefixed"
date: "2016-05-10T13:02:00-04:00"
categories: ["css"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=859301"
      title: "Bug 859301 - Unprefix css4 :dir"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1270406"
      title: "Bug 1270406 - remove pseudo class :-moz-dir after :dir is shipped"
---
The [`:dir`](https://developer.mozilla.org/en-US/docs/Web/CSS/:dir) CSS4 pseudo-class is now available in Firefox without the vender prefix. The prefixed `:-moz-dir` pseudo-class will be removed in the near future.
