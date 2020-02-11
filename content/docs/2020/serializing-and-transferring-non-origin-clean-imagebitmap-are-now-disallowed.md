---
title: "Serializing and transferring non-origin-clean `ImageBitmap` are now disallowed"
date: "2020-02-10T23:07:00-05:00"
categories: ["dom"]
tags: []
versions: ["74"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1604694"
      title: "Bug 1604694 - Disallow serializing and transferring non-origin-clean ImageBitmap"
    - url: "https://groups.google.com/a/chromium.org/d/topic/blink-dev/Z1XdYf6SjDU/discussion"
      title: "Intent to Deprecate and Remove: non-origin-clean ImageBitmap serialization and transferring"
---
An [`ImageBitmap`](https://developer.mozilla.org/docs/Web/API/ImageBitmap) could contain data from a cross-origin image that is not verified by the [Cross-Origin Resource Sharing](https://developer.mozilla.org/docs/Web/HTTP/CORS) (CORS) mechanism. Starting with Firefox 74 and [Chrome 80](https://www.chromestatus.com/feature/5728790883860480), for security reasons, such an `ImageBitmap` can no longer be serialized or transferred. Since this is a rarely used feature, according to a developer, the compatibility risk should be minimum.
