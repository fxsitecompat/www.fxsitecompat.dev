---
title: "Flash will be loaded only from HTTP(S) sites"
date: "2017-02-09T05:03:00-05:00"
categories: ["plugins", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1335475"
      title: "Bug 1335475 - Deny plugins from non-HTTP/HTTPS protocols"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/HdM-yCnhTYo/discussion"
      title: "Intent to implement and ship: only allow Flash on HTTP/HTTPS sites"
---
Firefox will soon prevent Flash content from being loaded from `file`, `ftp` or any other URL schemes except `http` and `https`. This change aims to improve security, given that a different [same-origin policy](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy) is applied to the `file` protocol, and loading Flash content from other minor protocols is usually not well-tested. The details of the change are not determined yet.
