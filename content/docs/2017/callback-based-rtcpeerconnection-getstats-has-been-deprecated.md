---
title: "Callback-based `RTCPeerConnection.getStats()` has been deprecated"
date: "2017-03-11T21:04:00-05:00"
categories: ["audio-video"]
tags: []
versions: ["53"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1323095"
      title: "Bug 1323095 - Add deprecation warnings to callback-based pc.getStats()"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1329762"
      title: "Bug 1329762 - Strengthen deprecation warning of legacy PeerConnection.getStats"
---
The callback-based `RTCPeerConnection.prototype.getStats` method, which provides a [`RTCStatsReport`](https://developer.mozilla.org/en-US/docs/Web/API/RTCStatsReport), has been removed from the WebRTC spec and will also be removed from Firefox in the near future. The Web Console on Firefox 53 and later shows a deprecation warning for the legacy version. Use the new [Promise version](https://w3c.github.io/webrtc-pc/#getstats-example) instead.
