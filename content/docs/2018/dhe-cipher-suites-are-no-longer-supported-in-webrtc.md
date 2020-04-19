---
title: "DHE cipher suites are no longer supported in WebRTC"
date: "2018-10-27T01:09:00-04:00"
categories: ["audio-video", "privacy-security"]
tags: []
releases: ["65", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1227519"
      title: "Bug 1227519 - Establish deprecation date for DHE cipher suites in WebRTC"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/5n16ltyShIE/discussion"
      title: "Intent to remove DHE ciphers in Fx 64 (Was: Intent to remove DHE ciphers from WebRTC DTLS handshake)"
---
The support for the following DHE cipher suites has been removed from WebRTC Datagram Transport Layer Security (DTLS) handshake, because those protocols are considered too weak. There are only a few uses of DHE at this time according to Mozilla's Telemetry, so the compatibility risk of the removal should be very low.

* `TLS_DHE_RSA_WITH_AES_128_CBC_SHA`
* `TLS_DHE_RSA_WITH_AES_256_CBC_SHA`
