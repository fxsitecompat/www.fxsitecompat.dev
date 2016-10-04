---
title: "`jar` protocol support has been disabled by default"
date: "2015-11-04T13:03:00-08:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["45"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1215235"
      title: "Bug 1215235 - Drop support for jar: URIs by default"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/CFd4w8GzdEI/discussion"
      title: "Intent to unship: jar: URIs from content"
aliases:
    - "/docs/2015/jar-protocol-support-will-be-removed/"
---
The `jar` protocol, that allows to directly link to a file in ZIP archives, is no longer available from Web content due to [security concerns](https://developer.mozilla.org/en-US/docs/Mozilla/Security/Security_and_the_jar_protocol). No other browsers support this Java archive protocol so far.

To enable the `jar` support for any reason on Firefox 45 and later, flip the `network.jar.block-remote-files` preference value to `false`. Otherwise, loading the `jar` protocol will lead to the `NS_ERROR_UNSAFE_CONTENT_TYPE` exception.

**Update**: Since [*IBM iNotes* is broken](https://bugzilla.mozilla.org/show_bug.cgi?id=1255139) due to this change, the `jar` protocol support has been temporarily restored with Firefox 45.0.1. On Firefox Nightly and Developer Edition, the `network.jar.block-remote-files` preference will remain `true`.
