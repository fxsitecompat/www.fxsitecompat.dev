---
title: "Support for `#RGBA` colour values may validate previously invalid values"
date: "2016-05-30T09:38:00-04:00"
categories: ["css"]
tags: []
releases: ["49", "52-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=567283"
      title: "Bug 567283 - Add support for 4 and 8 CSS hexcolor values (#RRGGBBAA and #RGBA)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1304810"
      title: "Bug 1304810 - Microsoft Dynamics CRM notes appear to be blank due to #0000 rgba hex parsing"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/00Tq2s58GwA/discussion"
      title: "Intent to implement and ship: #rgba and #rrggbbaa color syntax in CSS"
---
Firefox 49 has added the support for 4-digit (`#RGBA`) and 8-digit (`#RRGGBBAA`) hexadecimal notations for [RGBa colour values](https://developer.mozilla.org/docs/Web/CSS/color_value#rgba%28%29). Due to this change, previously invalid values could be valid, yielding unexpected results. A typical example is `#0000`, which is now parsed as [`transparent`](https://developer.mozilla.org/docs/Web/CSS/color_value#transparent_keyword). You may want to double check your stylesheets for such errors.

**Update**: *Microsoft Dynamics CRM 2016* is known to be affected because of `#0000` wrongly used for the text colour on a few elements.
