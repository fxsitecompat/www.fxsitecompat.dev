---
title: "Certain multi-column layouts may balance unevenly or lack elements randomly"
date: "2017-11-10T03:24:00-05:00"
categories: ["css"]
tags: []
versions: ["56"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1308876"
      title: "Bug 1308876 - Nested inline-blocks with matching width locks up browser due to O(2^depth) reflow performance"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1406619"
      title: "Bug 1406619 - Two-column layout balanced unevenly and nondeterministically since Firefox 56"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1411799"
      title: "Bug 1411799 - Content of ::before/after pseudo elements randomly disappears when display:inline-block and float are used"
---
Firefox 56 has introduced a regression on [CSS multi-column layouts](https://developer.mozilla.org/docs/Web/CSS/CSS_Columns) due to a performance enhancement. One report shows a two-column layout balanced unevenly. Another bug has been found ironically on this [FxSiteCompat.com](https://www.fxsitecompat.dev/en-CA/docs/) where `::before` pseudo-elements randomly disappear within a multi-column layout if combined with `display:inline-block` and `float:left`. Troublingly, the behaviour is capricious in both cases. Mozilla developers will look into the issues shortly.
