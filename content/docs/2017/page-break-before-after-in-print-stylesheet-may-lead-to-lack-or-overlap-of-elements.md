---
title: "`page-break-before`/`after` in print stylesheet may lead to lack or overlap of elements"
date: "2017-11-10T03:43:00-05:00"
categories: ["css"]
tags: []
versions: ["56"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1308876"
      title: "Bug 1308876 - Nested inline-blocks with matching width locks up browser due to O(2^depth) reflow performance"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1406291"
      title: "Bug 1406291 - floating table following quickly after page-break-after style is not printed"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1404868"
      title: "Bug 1406356 - overlapping content following page-break-before in Firefox 56"
---
Firefox 56 has introduced a printing regression due to a performance enhancement, which is actually the same cause as of a [multi-column layout regression](https://www.fxsitecompat.com/en-CA/docs/2017/certain-multi-column-layouts-may-balance-unevenly-or-lack-elements-randomly/) described separately.

When an element has the [`page-break-before`](https://developer.mozilla.org/en-US/docs/Web/CSS/page-break-before) or [`page-break-after`](https://developer.mozilla.org/en-US/docs/Web/CSS/page-break-after) property specified in the print stylesheet, the following elements may disappear or overlap with the previous element. These issues only affect the document's print output, so the page is still rendered properly within the browser. Mozilla developers will look into the issues shortly.
