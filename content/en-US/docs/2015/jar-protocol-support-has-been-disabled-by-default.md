---
title: "`jar` protocol support has been disabled by default"
date: "2015-11-04T13:03:00-08:00"
categories: ["networking"]
tags: []
versions: ["45"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1215235": "Bug 1215235 - Drop support for jar: URIs by default"
    "https://groups.google.com/d/topic/mozilla.dev.platform/CFd4w8GzdEI/discussion": "Intent to unship: jar: URIs from content"
aliases:
    - "/docs/2015/jar-protocol-support-will-be-removed/"
---
The `jar` protocol, that allows to directly link to a file in ZIP archives, is no longer available from Web content. No other browsers support this Java archive protocol so far. To enable the `jar` support for any reason on Firefox 45 and later, flip the `network.jar.block-remote-files` preference value.
