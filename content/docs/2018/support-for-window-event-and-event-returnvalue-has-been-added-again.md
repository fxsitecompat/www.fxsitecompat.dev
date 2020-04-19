---
title: "Support for `window.event` and `Event.returnValue` has been added again"
date: "2018-12-24T19:40:00-05:00"
categories: ["dom"]
tags: []
releases: ["66", "68-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=218415"
      title: "Bug 218415 - Request for window.event object added to DOM to ease cross browser scripting"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1452569"
      title: "Bug 1452569 - Implement Event's returnValue"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1479964"
      title: "Bug 1479964 - Tracking event.keyCode issue due to the implementation of window.event"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1496288"
      title: "Bug 1496288 - Ship Window.event, keyCode change, and keypress event handling changes"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/riVG9FqN9iM/discussion"
      title: "Intent to ship: window.event"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/IWLLJmoGroA/discussion"
      title: "Intent to ship: set keyCode or charCode of \"keypress\" event to the other's non-zero value"
---
Firefox 65 has re-added the support for the Internet Explorer-derived [`window.event`](https://developer.mozilla.org/docs/Web/API/Window/event) and [`Event.prototype.returnValue`](https://developer.mozilla.org/docs/Web/API/Event/returnValue) properties, which was once landed on [Firefox 63](https://www.fxsitecompat.dev/en-CA/docs/2018/support-for-event-returnvalue-has-been-added/) but soon disabled on non-Nightly channels due to several site compatibility issues.

In Firefox 65 and later, when the `keyCode` property of the `keypress` event is `0`, the value will be the same as `charCode`. Conversely, when `charCode` is `0`, it will be the same as `keyCode`. Although this mirroring behaviour matches other browsers and is expected to solve most of the compatibility issues, user agent sniffing might cause another issues like the *Closure Library*, which has already been [solved by Google](https://github.com/google/closure-library/issues/932).

Web developers are also discouraged to use these once-non-standard properties for browser detection.

**Update**: This change has been [postponed to Firefox 66](https://bugzilla.mozilla.org/show_bug.cgi?id=1520756) to deal with an [input issue](https://bugzilla.mozilla.org/show_bug.cgi?id=1514940) in *Confluence*'s comment editor.
