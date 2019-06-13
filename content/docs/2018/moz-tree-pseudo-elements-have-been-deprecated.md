---
title: "`::-moz-tree` pseudo-elements have been deprecated"
date: "2018-08-14T21:29:00-04:00"
categories: ["css"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1480054"
      title: "Bug 1480054 - Don't allow tree pseudos with arguments in content."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/gbzTmE4uvJk/discussion"
      title: "Intent to unship: ::-moz-tree pseudo-elements."
---
The following non-standard CSS pseudo-elements are now considered deprecated and disabled by default in Firefox Nightly and early Beta/DevEdition. Assuming no major issues arise, these pseudo-elements will be removed from all the channels in the near future.

* `::-moz-tree-cell`
* `::-moz-tree-cell-text`
* `::-moz-tree-checkbox`
* `::-moz-tree-column`
* `::-moz-tree-drop-feedback`
* `::-moz-tree-image`
* `::-moz-tree-indentation`
* `::-moz-tree-line`
* `::-moz-tree-row`
* `::-moz-tree-separator`
* `::-moz-tree-twisty`

**Update**: These pseudo-elements have been [removed with Firefox 64](https://www.fxsitecompat.dev/en-CA/docs/2018/display-moz-box-and-moz-tree-pseudo-elements-have-been-removed/).
