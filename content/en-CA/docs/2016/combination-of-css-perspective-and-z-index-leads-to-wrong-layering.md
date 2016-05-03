---
title: "Combination of CSS `perspective` and `z-index` leads to wrong layering"
date: "2016-05-03T14:05:00-04:00"
categories: ["css"]
tags: []
versions: ["46"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1269184"
      title: "Bug 1269184 - CSS perspective and z-index not layered properly on Firefox 46+, breaking site navigation on ESPN FC and ADS-B Exchange"
---
Firefox 46 has introduced a regression where an HTML element styled with both the [`perspective`](https://developer.mozilla.org/en-US/docs/Web/CSS/perspective) and [`z-index`](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index) CSS properties is not rendered with proper layering, resulting in an invisible site navigation, for example. *ESPN FC* and other sites are affected. Mozilla developers are working on the solution.
