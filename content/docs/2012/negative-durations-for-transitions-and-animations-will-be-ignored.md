---
title: "Negative durations for transitions and animations will be ignored"
date: "2012-10-09T06:00:00-04:00"
categories: ["css"]
tags: []
versions: ["16"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=773102"
      title: "Bug 773102 – transition-duration and animation-duration should reject negative values at parse time"
---
Previously, negative values specified for the [`transition-duration`](https://developer.mozilla.org/docs/Web/CSS/transition-duration) and [`animation-duration`](https://developer.mozilla.org/docs/Web/CSS/animation-duration) properties were interpreted as `0s`, the [initial value](https://developer.mozilla.org/docs/Web/CSS/initial_value). Such values are now considered invalid and the declaration itself will be ignored.
