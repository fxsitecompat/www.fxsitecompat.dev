---
title: "`:-moz-table-border-nonzero` pseudo-class has been removed"
date: "2017-02-28T23:43:00-05:00"
categories: ["css"]
tags: []
releases: ["54", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1341925"
      title: "Bug 1341925 - Restrict :-moz-table-border-nonzero pseudo-class to UA stylesheet"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/jtdC_pUmCew/discussion"
      title: "Intent to unship: \"-moz-table-border-non-zero\" pseudo-class outside UA stylesheet"
---
The non-standard, undocumented `:-moz-table-border-nonzero` pseudo-class for the `<table>` element is no longer available to web content. An alternate selector will be `[border]:not([border="0"])`.
