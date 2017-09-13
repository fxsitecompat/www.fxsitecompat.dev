---
title: "`window.content` has been removed"
date: "2017-09-13T07:19:00-04:00"
categories: ["dom"]
tags: []
versions: ["57"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=864845"
      title: "Bug 864845 - Make window.content chrome-only"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/Tmbs-wFwHzo/discussion"
      title: "Intent to unship: Visibility of window.content to untrusted code"
---
The non-standard [`window.content`](https://developer.mozilla.org/en-US/docs/Web/API/Window/content) object is no longer available from web content on Firefox 57 and later. This object isn't useful because it's just an alias of [`window.top`](https://developer.mozilla.org/en-US/docs/Web/API/Window/top) or simply [`window`](https://developer.mozilla.org/en-US/docs/Web/API/Window) in many cases, but it may have been misused for browser detection purposes on the web, like [`window.controllers`] (https://developer.mozilla.org/en-US/docs/Web/API/Window/controllers) that was once removed with [Firefox 29](https://www.fxsitecompat.com/en-CA/docs/2014/window-content-controllers-pkcs11-and-loadstatus-have-been-removed/) but added back to retain backward compatibility. Web developers should always avoid using these kind of non-standard features.
