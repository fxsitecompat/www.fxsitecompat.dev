---
title: "HTTP Public Key Pinning is no longer supported"
date: "2019-11-14T16:54:00-05:00"
categories: ["networking", "privacy-security"]
tags: []
releases: ["72"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1412438"
      title: "Bug 1412438 - consider removal of HTTP Public Key Pinning (HPKP)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/AyMlrNHYepE/discussion"
      title: "intent to unship: HPKP (dynamic key pinning)"
---
Firefox 72 has dropped the support for [HTTP Public Key Pinning](https://developer.mozilla.org/docs/Web/HTTP/Public_Key_Pinning) (HPKP) because of the low adoption rate and interoperability risk. Since Google Chrome has already [removed the support](https://www.chromestatus.com/feature/5903385005916160) with version 72 and the security feature is not supported by other browsers, any misconfigured or temporarily compromised site could be blocked only in Firefox, resulting in a degraded user experience. The `Public-Key-Pins` HTTP response header will be simply ignored from now on.
