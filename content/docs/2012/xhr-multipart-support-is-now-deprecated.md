---
title: "XHR multipart support is now deprecated"
date: "2012-12-29T08:29:30-05:00"
categories: ["dom"]
tags: []
versions: ["20"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=844792"
      title: "Bug 844792 – Warn about the upcoming removal of multipart support in XHR"
---
Support for the `multipart` property and `multipart/x-mixed-replace` responses in [`XMLHttpRequest`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest) has been deprecated. This was a Firefox-only feature that was never standardized, therefore it will be [removed from Firefox 22](https://www.fxsitecompat.dev/en-CA/docs/2013/xhr-multipart-response-support-has-been-removed/). [Server-Sent Events](https://developer.mozilla.org/docs/Server-sent_events), [Web Sockets](https://developer.mozilla.org/docs/WebSockets) or inspecting `responseText` from progress events can be used instead.

**Update**: The multipart support has been [removed with Firefox 22](https://www.fxsitecompat.dev/en-CA/docs/2013/xhr-multipart-response-support-has-been-removed/).
