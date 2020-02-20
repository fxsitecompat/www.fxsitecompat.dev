---
title: "DTLS 1.0 support in WebRTC has been removed"
date: "2020-02-19T20:27:00-05:00"
categories: ["audio-video", "networking", "privacy-security"]
tags: []
versions: ["75"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1615445"
      title: "Bug 1615445 - Set minimum DTLS version to 1.2"
    - url: "https://blog.mozilla.org/webrtc/removing-old-versions-of-dtls/"
      title: "Removing Old Versions of DTLS - Advancing WebRTC"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/wUoBf0FqqcE/discussion"
      title: "Intent to unship: DTLS 1.0 for WebRTC"
---
Firefox 75 has bumped the default minimum version of [Datagram Transport Layer Security](https://developer.mozilla.org/docs/Glossary/DTLS) (DTLS) in WebRTC to 1.2. According to Mozilla, more than 98% of WebRTC services have already adopted DTLS 1.2. If you are still using DTLS 1.0, it’s time to upgrade.
