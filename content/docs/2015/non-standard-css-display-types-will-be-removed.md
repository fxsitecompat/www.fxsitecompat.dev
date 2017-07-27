---
title: "Non-standard CSS `display` types will be removed"
date: "2015-10-27T17:21:00-07:00"
categories: ["css"]
tags: []
versions: ["future"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=879275"
      title: "Bug 879275 - Consider turning off -moz-box display types in untrusted stylesheets"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=914360"
      title: "Bug 914360 - Do not expose XUL Grid (display: -moz-grid;) to Web content"
---
The non-standard CSS [`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display) property values, originally intended for [XUL](https://developer.mozilla.org/en-US/docs/Mozilla/Tech/XUL) used by Firefox, will no longer be available from Web content. This includes `-moz-box`, `-moz-deck`, `-moz-grid`, `-moz-grid-group`, `-moz-grid-line`, `-moz-groupbox`, `-moz-inline-box`, `-moz-inline-grid`, `-moz-inline-stack`, `-moz-popup` and `-moz-stack`. Use the [standard flexboxes](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes) instead.
