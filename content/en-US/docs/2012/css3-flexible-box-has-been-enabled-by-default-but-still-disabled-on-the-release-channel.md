---
title: "CSS3 Flexible Box has been enabled by default, but still disabled on the Release channel"
date: "2012-12-29T08:29:30-05:00"
categories: ["css"]
tags: []
versions: "20"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=783409": "Bug 783409 – Turn on CSS flexbox in builds by default (by enabling pref, build flag, etc)"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=841873": "Bug 841873 – Make flexbox automatically preffed off by default, in release builds"
---
The new [Flexible Box (flexbox)](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Flexible_boxes) implemented in [Firefox 18](https://developer.mozilla.org/en-US/docs/Firefox_18_for_developers) is now available without having to edit a hidden preference. Note that it's not compatible with the traditional prefixed implementation such as [`-moz-box-flex`](https://developer.mozilla.org/en-US/docs/Web/CSS/-moz-box-flex).

Although developers can now test the flexbox with [Aurora](http://www.mozilla.org/en-US/firefox/aurora/) or [Beta](http://www.mozilla.org/en-US/firefox/beta/), **this feature will be keep disabled on the Release channel until it's ready for production**.
