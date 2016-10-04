---
title: "SHA-1 support has been deprecated"
date: "2014-12-19T11:15:21-05:00"
categories: ["privacy-security"]
tags: []
versions: ["36"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1068949"
      title: "Bug 1068949 – Add SHA-1 warnings to web console for end entities"
---
The support for SSL certificates using the [weak SHA-1 hash algorithm](https://developer.mozilla.org/en-US/docs/Security/Weak_Signature_Algorithm) has been deprecated. The [Web Console will log a warning](https://developer.mozilla.org/en-US/docs/Tools/Web_Console#Security_warnings_and_errors) when a SHA-1 certificate is found.

**Update** The SHA-1 support will be [disabled as early as July 2016](https://www.fxsitecompat.com/en-CA/docs/2015/sha-1-certificate-support-will-be-disabled-as-early-as-july-2016/).
