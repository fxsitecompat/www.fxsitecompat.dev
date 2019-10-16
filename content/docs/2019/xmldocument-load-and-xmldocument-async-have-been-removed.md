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
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1546112"
      title: "Bug 1546112 - Remove the code for XMLDocument.load/async if possible"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1569102"
      title: "Bug 1569102 - xmldocument load type error"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/0T4l3yaP3g4/discussion"
      title: "Intent to unship: XMLDocument.load and XMLDocument.async APIs"
---
Firefox 68 has dropped the support for the [`load`](https://developer.mozilla.org/docs/Web/API/XMLDocument/load) method and [`async`](https://developer.mozilla.org/docs/Web/API/XMLDocument/async) property from the `XMLDocument` interface. This was a very old, non-standard API that could be used to retrieve a remote XML document synchronously or asynchronously, but was later superseded by `XMLHttpRequest`. It was never standardized or implemented by other browsers than Firefox. However, Mozilla still sees a small usage of the API (~0.01%) so web developers are encouraged to scan any legacy code and use `XMLHttpRequest` or `fetch()` instead.

**Update**: This change has been reverted in Firefox ESR 68 ([68.1.0](https://www.mozilla.org/en-US/firefox/68.1.0/releasenotes/) and later) to maintain the compatibility with legacy applications. The relevant code has been completely removed with Firefox 71, so any application using the old feature still has to be updated for Firefox ESR 78 shipping in June 2020.
