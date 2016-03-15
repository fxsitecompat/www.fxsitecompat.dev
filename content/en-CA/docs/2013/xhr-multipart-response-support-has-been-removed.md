---
title: "XHR multipart response support has been removed"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
versions: ["22"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=843508"
      title: "Bug 843508 – Remove support for multipart XHR responses"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/iuKw5doD5Ho/discussion"
      title: "Chrome removed support for multipart/x-mixed-replace documents. We should too."
---
Support for the `multipart` property and `multipart/x-mixed-replace` responses, [deprecated since Firefox 20](https://www.fxsitecompat.com/en-CA/docs/2012/xhr-multipart-support-is-now-deprecated/), has been removed from [`XMLHttpRequest`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest). This was a Firefox-only feature that was never standardized. [Server-Sent Events](https://developer.mozilla.org/en-US/docs/Server-sent_events), [Web Sockets](https://developer.mozilla.org/en-US/docs/WebSockets) or inspecting `responseText` from progress events can be used instead.
