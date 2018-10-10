---
title: "`display:-moz-box` and `::-moz-tree` pseudo-elements have been removed"
date: "2018-10-10T07:46:00-04:00"
categories: ["css"]
tags: []
versions: ["64"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1496961"
      title: "Bug 1496961 - Let some XUL unshipping prefs ride the trains."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/C83tct9EPAk/discussion"
      title: "Intent to unship: display: -moz-box and display: -moz-inline-box from content pages."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/gbzTmE4uvJk/discussion"
      title: "Intent to unship: ::-moz-tree pseudo-elements."
---
The non-standard `-moz-box` and `-moz-inline-box` values for the CSS `display` property, [deprecated since Firefox 63](https://www.fxsitecompat.com/en-CA/docs/2018/display-moz-box-and-display-moz-inline-box-have-been-deprecated/), as well as the following non-standard CSS pseudo-elements, also [deprecated since Firefox 63](https://www.fxsitecompat.com/en-CA/docs/2018/moz-tree-pseudo-elements-have-been-deprecated/), are no longer available from web content as of Firefox 64.

Those were created for the Firefox user interface written in now-deprecated [XUL](https://developer.mozilla.org/docs/Mozilla/Tech/XUL) and supported by no other browsers. No compatibility issues due to the removal have been reported so far.

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
