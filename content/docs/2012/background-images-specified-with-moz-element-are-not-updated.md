---
title: "Background images specified with `-moz-element()` are not updated"
date: "2012-12-03T03:54:45-05:00"
categories: ["css"]
tags: []
releases: ["19", "24-esr"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=909157"
      title: "Bug 909157 – -moz-element background fails to update after image reloads"
---
CSS background images specified with the [`-moz-element`](https://developer.mozilla.org/docs/Web/CSS/-moz-element) function are not updated when the [`background-image`](https://developer.mozilla.org/docs/Web/CSS/background-image) of the source element is dynamically changed. This is a regression since Firefox 19, which has been fixed with Firefox 26.
