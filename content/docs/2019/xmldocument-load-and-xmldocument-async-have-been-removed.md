---
title: "`XMLDocument.load()` and `XMLDocument.async` have been removed"
date: "2019-05-28T01:20:00-04:00"
categories: ["dom"]
tags: []
versions: ["68"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=332175"
      title: "Bug 332175 - Drop XMLDocument.load() support"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1328138"
      title: "Bug 1328138 - Remove XMLDocument's async IDL attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/0T4l3yaP3g4/discussion"
      title: "Intent to unship: XMLDocument.load and XMLDocument.async APIs"
---
Firefox 68 has dropped the support for the [`load`](https://developer.mozilla.org/docs/Web/API/XMLDocument/load) method and [`async`](https://developer.mozilla.org/docs/Web/API/XMLDocument/async) property from the `XMLDocument` interface. This was a very old, non-standard API that could be used to retrieve a remote XML document synchronously or asynchronously, but was later superseded by `XMLHttpRequest`. It was never standardized or implemented by other browsers than Firefox. However, Mozilla still sees a small usage of the API (~0.01%) so web developers are encouraged to scan any legacy code and use `XMLHttpRequest` or `fetch()` instead.
