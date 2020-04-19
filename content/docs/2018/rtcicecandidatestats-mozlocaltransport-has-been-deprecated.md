---
title: "`RTCIceCandidateStats.mozLocalTransport` has been deprecated"
date: "2018-10-23T16:20:00-04:00"
categories: ["audio-video", "dom"]
tags: []
releases: ["64", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1435789"
      title: "Bug 1435789 - Deprecate RTCIceCandidateStats.mozLocalTransport and add protocol and relayProtocol"
---
The non-standard `mozLocalTransport` property on the `RTCIceCandidateStats` dictionary, retuned by [`RTCPeerConnection.getStats()`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection/getStats) and similar methods, is now considered deprecated and will be removed in the near future. Use the standardized `relayProtocol` property instead.

**Update**: The property has been removed with [Firefox 65](https://www.fxsitecompat.dev/en-CA/docs/2018/rtcicecandidatestats-has-been-updated-to-the-latest-spec/).
