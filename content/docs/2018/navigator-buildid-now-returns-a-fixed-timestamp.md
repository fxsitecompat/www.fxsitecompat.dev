---
title: "`navigator.buildID` now returns a fixed timestamp"
date: "2018-10-10T03:44:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["64"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=583181"
      title: "Bug 583181 - Don't reveal navigator.buildID to every site on the web"
aliases:
    - "/en-CA/docs/2015/navigator-buildid-will-be-removed/"
    - "/en-CA/docs/2018/navigator-buildid-has-been-removed/"
---
The non-standard [`navigator.buildID`](https://developer.mozilla.org/docs/Web/API/Navigator/buildID) property, that returns the 14-digit build identifier of Firefox, is now fixed at `"20181001000000"`. The change has been made in an effort to better protect user privacy.

Since [Firefox 16](https://www.fxsitecompat.dev/en-CA/docs/2012/ua-string-no-longer-contains-patch-level-version-number/), the minor version number has been excluded from the browser's user agent (UA) string that can be obtained with the `navigator.userAgent` property or the `User-Agent` HTTP header. Also, since [Firefox 25](https://www.fxsitecompat.dev/en-CA/docs/2015/build-id-in-ua-string-is-now-frozen-at-20100101/), the build ID in the UA string has been frozen at `20100101`. However, the `navigator.buildID` property had kept exposing the actual build ID that varied by the minor release of Firefox and platform, that could be a fingerprinting vector.

Given that the property may be used by some websites for browser detection, it has been fixed instead of being removed, though exposing a non-standard property to web content is not ideal.

**Update**: The earlier version of this article said the property was removed, but it has actually been kept to avoid potential compatibility issues. We have corrected the title and description.
