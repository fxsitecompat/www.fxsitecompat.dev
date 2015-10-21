---
title: "Key frame rule declarations with `!important` will be ignored"
date: "2012-12-03T03:54:45-05:00"
categories: ["css"]
tags: []
versions: ["19"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=784466": "Bug 784466 – [css3-animations] we should drop declarations in keyframe rules that have !important"
---
Following the latest [CSS3 animations](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Using_CSS_animations) spec, key frame rule declarations with the `!important` keyword are now be ignored and parse errors will be returned.
