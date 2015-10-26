---
title: "`jar` protocol support will be removed"
date: "2015-10-25T17:34:00-07:00"
categories: ["networking"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1215235": "Bug 1215235 - Drop support for jar: URIs by default"
    "https://groups.google.com/d/topic/mozilla.dev.platform/CFd4w8GzdEI/discussion": "Intent to unship: jar: URIs from content"
---
The `jar` protocol, that allows to directly link to a file in ZIP archives, will no longer be available from Web content. No other browsers support this Java archive protocol so far.
