---
title: "Flash can now be loaded only from HTTP/HTTPS"
date: "2017-03-10T16:44:00-05:00"
categories: ["plugins", "privacy-security"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1335475"
      title: "Bug 1335475 - Deny plugins from non-HTTP/HTTPS protocols"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/HdM-yCnhTYo/discussion"
      title: "Intent to implement and ship: only allow Flash on HTTP/HTTPS sites"
aliases:
    - "/docs/2017/flash-will-be-loaded-only-from-https-sites/"
---
Firefox 55 and later will prevent Flash content from being loaded from `file`, `ftp` or any other URL schemes except `http` and `https`. This change aims to improve security, because a different [same-origin policy](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy) is applied to the `file` protocol, and loading Flash content from other minor protocols is usually not well-tested.

Developers can still test local Flash files by flipping the hidden `plugins.http_https_only` preference through [`about:config`](https://support.mozilla.org/kb/about-config-editor-firefox), but you may rather want to set up a local web server to do so.
