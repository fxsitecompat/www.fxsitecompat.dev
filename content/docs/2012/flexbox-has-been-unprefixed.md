---
title: "Flexbox has been unprefixed"
date: "2012-12-03T03:54:45-05:00"
categories: ["css"]
tags: []
releases: ["19", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=801098"
      title: "Bug 801098 – Unprefix CSS3 flexbox"
---
The [CSS3 flexible boxes (flexbox)](https://developer.mozilla.org/docs/Web/Guide/CSS/Flexible_boxes) implementation has been prefixed. From now on, use the related properties and keywords without `moz` prefix. Note that the flexbox is still disabled by default in Firefox 19. If you'd like to test the feature, open `about:config` and change the value of `layout.css.flexbox.enabled` to `true`.
