---
title: "`display:-moz-box` and `display:-moz-inline-box` have been deprecated"
date: "2018-08-14T21:04:00-04:00"
categories: ["css"]
tags: []
versions: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1477553"
      title: "Bug 1477553 - Hide display: -moz-box and display: -moz-inline-box from content in Nightly / early beta."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/C83tct9EPAk/discussion"
      title: "Intent to unship: display: -moz-box and display: -moz-inline-box from content pages."
---
The non-standard `-moz-box` and `-moz-inline-box` values for the CSS `display` property are now considered deprecated and disabled by default in Firefox Nightly and early Beta/DevEdition. Assuming no major issues arise, these values will be removed from all the channels in the near future.

Note that other non-standard values for the `display` property, including `-moz-grid` and `-moz-inline-grid`, have already been [dropped with Firefox 62](https://www.fxsitecompat.dev/en-CA/docs/2018/most-of-non-standard-css-display-values-have-been-dropped/).

**Update**: These values have been [removed with Firefox 64](https://www.fxsitecompat.dev/en-CA/docs/2018/display-moz-box-and-moz-tree-pseudo-elements-have-been-removed/).
