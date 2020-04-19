---
title: "DTLS 1.0 support in WebRTC has been removed"
date: "2020-02-19T20:27:00-05:00"
categories: ["audio-video", "networking", "privacy-security"]
tags: []
releases: ["75"]
statuses: "postponed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1615445"
      title: "Bug 1615445 - Set minimum DTLS version to 1.2"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1623511"
      title: "Bug 1623511 - Turn DTLS 1.0 back on to prevent sites breaking during Covid-19 traffic increase"
    - url: "https://blog.mozilla.org/webrtc/removing-old-versions-of-dtls/"
      title: "Removing Old Versions of DTLS - Advancing WebRTC"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/wUoBf0FqqcE/discussion"
      title: "Intent to unship: DTLS 1.0 for WebRTC"
---
Firefox 75 has bumped the default minimum version of [Datagram Transport Layer Security](https://developer.mozilla.org/docs/Glossary/DTLS) (DTLS) in WebRTC to 1.2. According to Mozilla, more than 98% of WebRTC services have already adopted DTLS 1.2. If you are still using DTLS 1.0, it’s time to upgrade.

**Update**: Mozilla is going to temporarily re-enable the DTLS 1.0 support in Firefox 75 Beta. This is because many people are currently forced to work at home and relying on video conference solutions amid the novel coronavirus (COVID-19) outbreak, but one of these services called *Jitsi* doesn’t support DTLS 1.2 yet. Also due to COVID-19, Google has [postponed the release of Chrome 82](https://blog.chromium.org/2020/03/upcoming-chrome-releases.html) that would [remove their DTLS 1.0 support](https://bugs.chromium.org/p/webrtc/issues/detail?id=10261). We’ll update this note when the situation has changed.
