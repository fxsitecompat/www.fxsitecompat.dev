---
title: "Setting cookies with `<meta http-equiv>` will no longer be allowed"
date: "2018-06-05T11:29:00-04:00"
categories: ["html", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1457503"
      title: "Bug 1457503 - Remove <meta http-equiv=set-cookie> support"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/AV_jwxqWdd0/discussion"
      title: "Intent to unship http-equiv cookies"
---
The HTML [`<meta>`](https://developer.mozilla.org/docs/Web/HTML/Element/meta) element provides an equivalent ability to sending certain HTTP response headers via the `http-equiv` attribute, which can even be used to set new cookies or override existing cookies.

```html
<meta http-equiv="Set-Cookie" content="key=value">
```

In an effort to mitigate the risk of cross-site scripting (XSS) attacks, this legacy behaviour has been removed from the latest HTML spec. [Google Chrome 65](https://bugs.chromium.org/p/chromium/issues/detail?id=767813) has already dropped the support in March 2018, and Firefox will follow soon.

Web developers are encouraged to use the standard [`Set-Cookie`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) HTTP header with the `HttpOnly`, `Secure` and `SameSite` directives to increase security.
