---
title: "3-valued CSS position is no longer supported except for `background-position`"
date: "2019-07-11T23:27:00-04:00"
categories: ["css"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1559276"
      title: "Bug 1559276 - Retiring support for 3-valued <position> (excluding background)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/zZ9FMk4OAsc/discussion"
      title: "Intent to unship: 3-valued position syntax from <object-position>, <perspective-origin>, <mask-position>"
---
Firefox 70 has dropped the support for the 3-valued position syntax for the `object-position`, `perspective-origin` and `mask-position` properties as well as the `circle` and `ellipse` shape functions, according to the current [CSS Values spec](https://drafts.csswg.org/css-values-4/#position). Only the 1, 2 or 4-valued syntax can be used from now on, though the `background-position` property still accepts the 3-valued syntax like `left 10px top`.

[Google Chrome](https://www.chromestatus.com/feature/5116559680864256) has made the same change in version 68.
