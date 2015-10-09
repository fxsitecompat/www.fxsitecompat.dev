---
title: "`dialog` option for `window.open()` is no longer supported"
date: "2015-10-06T00:25:00-04:00"
categories: ["dom"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1095236": "Bug 1095236 - [e10s] window.open(..., ..., \"dialog=1\") breaks with e10s enabled"
    "https://groups.google.com/d/topic/mozilla.dev.platform/cDpULPod8nQ/discussion": "mozilla.dev.platform: dialog=1 for window.open from content"
    "https://groups.google.com/d/topic/mozilla.dev.platform/gUORXMzvH1Y/discussion": "mozilla.dev.platform: Intent to unship: dialog=1 for window.open from web content"
---
The `dialog` option for the [`window.open`](https://developer.mozilla.org/en-US/docs/Web/API/Window/open) method is no longer available from Web content. This non-standard feature, that removed the minimize, maximize and restore buttons from the window's titlebar, had only been supported by Firefox and other Gecko-based browsers for Windows.
