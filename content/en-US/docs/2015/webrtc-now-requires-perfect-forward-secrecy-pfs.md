---
title: "WebRTC now requires Perfect Forward Secrecy (PFS)"
date: "2015-02-27T04:21:22-05:00"
categories: ["privacy-security"]
tags: []
versions: "38"
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1052610": "Bug 1052610 – WebRTC: Allow more ciphers for DTLS 1.2 in Firefox Nightly 34.0a1 (cannot perform DTLS with OpenSSL)"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1134437": "Bug 1134437 – Delay move to PFS cipher suites"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1158343": "Bug 1158343 – Temporarily re-enable TLS_RSA_WITH_AES_128_CBC_SHA for WebRTC"
---
Starting with Firefox 38, [WebRTC](https://developer.mozilla.org/en-US/docs/Web/Guide/API/WebRTC) requires one of the Perfect Forward Secrecy (PFS) cipher suites to make communicatons safer. See the [Mozilla Hacks blog](https://hacks.mozilla.org/2015/02/webrtc-requires-perfect-forward-secrecy-pfs-starting-in-firefox-38/) for details. Due to an interoperability issue on the *Facebook Messenger*, the `TLS_RSA_WITH_AES_128_CBC_SHA` suite has been temporarily re-enabled and will be disabled again with Firefox 39.
