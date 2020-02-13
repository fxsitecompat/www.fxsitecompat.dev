---
title: "`X-Content-Type-Options:nosniff` is now enforced even if `Content-Type` is not given"
date: "2020-02-12T23:28:00-05:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["75"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1594766"
      title: "Bug 1594766 - Decide whether to continue ignoring XCTO Nosniff when Content Type is Empty, or to enforce"
---
Since [Firefox 72](https://www.fxsitecompat.dev/en-CA/docs/2019/x-content-type-options-nosniff-now-applies-to-top-level-documents-causing-some-pages-to-be-downloaded/), the [`X-Content-Type-Options`](https://developer.mozilla.org/docs/Web/HTTP/Headers/X-Content-Type-Options) HTTP response header has been applied to top-level documents, but to mitigate the compatibility risk, the `nosniff` directive would be ignored when the `Content-Type` header is empty or not provided.

This workaround has been removed with Firefox 75 as Mozilla’s Telemetry has proved there’s no real risk. Still, web developers may want to be aware of the change because the `nosniff` enforcement causes HTML pages to be downloaded due to a misconfiguration of the server or application.
