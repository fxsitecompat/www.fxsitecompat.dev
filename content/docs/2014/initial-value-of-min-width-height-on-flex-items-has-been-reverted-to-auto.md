---
title: "Initial value of `min-width`/`height` on flex items has been reverted to `auto`"
date: "2014-09-01T22:12:15-04:00"
categories: ["css"]
tags: []
versions: ["34"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=984711"
      title: "Bug 984711 – Add back \"min-width:auto\" / \"min-height:auto\" for flex items"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1015474"
      title: "Bug 1015474 – Update min-width:auto/min-height:auto support to match updated flexbox spec language"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1057683"
      title: "Bug 1057683 – http://i100.independent.co.uk/ is broken in Nightly, due to the new \"min-height:auto\" flex item behavior (from flexbox spec change)"
---
Since [Firefox 22](https://www.fxsitecompat.com/en-CA/docs/2013/initial-value-for-min-width-and-min-height-has-been-changed-back-to-0-even-on-flex-items/), the [initial value](https://developer.mozilla.org/docs/Web/CSS/initial_value) of the [`min-width`](https://developer.mozilla.org/docs/Web/CSS/min-width) and [`min-height`](https://developer.mozilla.org/docs/Web/CSS/min-height) properties has been `0` even on [flex items](https://developer.mozilla.org/docs/Web/Guide/CSS/Flexible_boxes). According to the latest CSS Flexible Box Layout Module spec, this value has been changed back to [`auto`](https://developer.mozilla.org/docs/Web/CSS/auto) which will be calculated to the minimum item (`min-content`) size in a flexbox, while it's still `0` on non-flex items. If your style has any flex items, you may want to test the page with [Firefox Aurora](https://www.mozilla.org/firefox/channel/#aurora) and explicitly define `min-height:0` to keep the behaviour as before.
