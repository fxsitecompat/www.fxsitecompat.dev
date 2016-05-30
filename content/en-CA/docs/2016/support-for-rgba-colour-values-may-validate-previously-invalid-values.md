---
title: "Support for `#RGBA` colour values may validate previously invalid values"
date: "2016-05-30T09:38:00-04:00"
categories: ["css"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=567283"
      title: "Bug 567283 - Add support for 4 and 8 CSS hexcolor values (#RRGGBBAA and #RGBA)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/00Tq2s58GwA/discussion"
      title: "Intent to implement and ship: #rgba and #rrggbbaa color syntax in CSS"
---
Firefox 49 has added the support for 4-digit (`#RGBA`) and 8-digit (`#RRGGBBAA`) hexadecimal notations for [RGBa colour values](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value#rgba%28%29). Due to this change, previously invalid values could be valid, yielding unexpected results. A typical example is `#0000`, which is now parsed as [`transparent`](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value#transparent_keyword). You may want to double check your stylesheets for such errors.
