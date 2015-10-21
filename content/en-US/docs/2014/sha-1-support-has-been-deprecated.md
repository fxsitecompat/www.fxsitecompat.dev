---
title: "SHA-1 support has been deprecated"
date: "2014-12-19T11:15:21-05:00"
categories: ["privacy-security"]
tags: []
versions: ["36"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1068949": "Bug 1068949 – Add SHA-1 warnings to web console for end entities"
---
The support for SSL certificates using the [weak SHA-1 hash algorithm](https://developer.mozilla.org/en-US/docs/Security/Weak_Signature_Algorithm) has been deprecated. The [Web Console will log a warning](https://developer.mozilla.org/en-US/docs/Tools/Web_Console#Security_warnings_and_errors) when a SHA-1 certificate is found.
