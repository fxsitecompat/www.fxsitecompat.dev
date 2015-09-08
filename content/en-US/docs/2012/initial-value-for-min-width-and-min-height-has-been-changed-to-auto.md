---
title: "Initial value for `min-width` and `min-height` has been changed to `auto`"
date: "2012-12-03T03:53:26-05:00"
categories: ["css"]
tags: []
versions: "18"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=763689": "Bug 763689 – New initial value for \"min-width\" & \"min-height\": auto"
---
The [`min-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/min-width) and [`min-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/min-height) properties now take the [`auto`](https://developer.mozilla.org/en-US/docs/Web/CSS/auto) keyword as their [initial value](https://developer.mozilla.org/en-US/docs/Web/CSS/initial_value). For the [flexible boxes (flexbox)](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Flexible_boxes), that has been introduced in Firefox 18 but disabled by default, this `auto` keyword indicates the minimum item (`min-content`) in a flexbox. For the other elements, it has no effect as it resolves to `0` as before.
