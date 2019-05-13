---
title: "`-moz-binding` CSS property has been removed"
date: "2019-05-13T03:25:00-04:00"
categories: ["css"]
tags: []
versions: ["67"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1523712"
      title: "Bug 1523712 - Restrict parsing of -moz-binding to chrome and UA sheets."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/TR1_24OldK8/discussion"
      title: "Intent to unship: -moz-binding CSS property from content."
---
The `-moz-binding` CSS property, which was intended for internal use in Firefox to attach now-deprecated XML Binding Language (XBL) to an element, is no longer available from web content. It could be previously used for CSS hacks targeting Firefox on the web, but will be ignored on Firefox 67 and later.
