---
title: "Initial value for `min-width` and `min-height` has been changed back to `0` (even on flex items)"
date: "2013-02-24T03:44:31-05:00"
categories: ["css"]
tags: []
versions: ["22", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=848539"
      title: "Bug 848539 – Remove support for \"min-width: auto\" and \"min-height: auto\", since they\'re being dropped from flexbox spec"
---
Since [Firefox 18](https://www.fxsitecompat.dev/en-CA/docs/2012/initial-value-for-min-width-and-min-height-has-been-changed-to-auto/), the [`min-width`](https://developer.mozilla.org/docs/Web/CSS/min-width) and [`min-height`](https://developer.mozilla.org/docs/Web/CSS/min-height) properties have taken the [`auto`](https://developer.mozilla.org/docs/Web/CSS/auto) keyword as their [initial value](https://developer.mozilla.org/docs/Web/CSS/initial_value), which computed to `0` in most cases but had [special behaviour on flex items](https://www.w3.org/TR/2012/CR-css3-flexbox-20120918/#min-size-auto). This value was introduced in a previous version of the CSS [flexible box (flexbox)](https://developer.mozilla.org/docs/Web/Guide/CSS/Flexible_boxes) spec, but a subsequent version of the spec [removed the value](https://dvcs.w3.org/hg/csswg/rev/9437131b3d6e#l1.86). Consequently, the initial value of these properties has been restored to `0`, as defined in [CSS 2.1](https://www.w3.org/TR/CSS2/visudet.html#min-max-widths), and [`auto`](https://developer.mozilla.org/docs/Web/CSS/auto) is no longer recognized as a valid value.
