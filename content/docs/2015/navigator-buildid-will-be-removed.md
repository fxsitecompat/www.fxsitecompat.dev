---
title: "`navigator.buildID` will be removed"
date: "2015-10-25T21:43:00-07:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["64"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=583181"
      title: "Bug 583181 - Don't reveal navigator.buildID to every site on the web"
---
The non-standard [`navigator.buildID`](https://developer.mozilla.org/docs/Web/API/Navigator/buildID) property, that returns the build identifier of Firefox, is considered to be removed to protect user privacy, because the 14-digit identifier data could be used for fingerprinting.

Since [Firefox 16](https://www.fxsitecompat.com/en-CA/docs/2012/ua-string-no-longer-contains-patch-level-version-number/), the minor version number has been excluded from the browser's user agent (UA) string that can be obtained with the `navigator.userAgent` property. Also, since [Firefox 25](https://www.fxsitecompat.com/en-CA/docs/2015/build-id-in-ua-string-is-now-frozen-at-20100101/), the build ID in the UA string has been frozen at `20100101`. However, the `navigator.buildID` property still exposes the actual build identifier that varies by the minor release of Firefox and platform, that can be a fingerprinting factor.

**Update**: Mozilla engineers are planning to drop the property from Firefox 64.
