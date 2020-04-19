---
title: "`box-sizing:padding-box` has been removed"
date: "2016-06-19T11:57:00-04:00"
categories: ["css"]
tags: []
releases: ["50", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1166728"
      title: "Bug 1166728 - remove box-sizing: padding-box"
aliases:
    - "/en-CA/docs/2015/box-sizing-padding-box-will-be-removed/"
---
The [`box-sizing`](https://developer.mozilla.org/docs/Web/CSS/box-sizing) CSS property no longer takes `padding-box` since the value has been removed from the spec. Use `border-box` instead.
