---
title: "`image/webp` has been added to default HTTP `Accept` header"
date: "2019-11-16T11:43:00-05:00"
categories: ["networking"]
tags: []
versions: ["72"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1544231"
      title: "Bug 1544231 - Missing 'image/webp' in default navigation value of the 'Accept' header"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/UTHTGok5x4o/discussion"
      title: "Intent to ship: Add image/webp to default Accept header"
---
When [Firefox 65](https://www.fxsitecompat.dev/en-CA/docs/2018/webp-image-support-has-been-added/) introduced the WebP image support, `image/webp` was added to the HTTP `Accept` request header for both default navigation (normal HTML page load) and images. Then, Firefox 66 removed it from the default `Accept` header, because the value didn't align with the [Fetch spec](https://fetch.spec.whatwg.org/#fetching).

While the spec hasn't changed yet, given that Google Chrome continues sending `image/webp` and various sites are using it for server-side WebP support detection, Firefox 72 has added `image/webp` again to the default `Accept` header. The new value will look like this:

```
text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8
```
