---
title: "`RTCInboundRTPStreamStats.mozRtt` has been unprefixed"
date: "2017-06-07T08:50:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["55", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1344970"
      title: "Bug 1344970 - Rename mozRtt stat to roundTripTime and change behavior to match spec"
---
The `mozRtt` property on the [`RTCInboundRTPStreamStats`](https://w3c.github.io/webrtc-stats/#inboundrtpstats-dict*) dictionary has been renamed to `roundTripTime` according to the latest WebRTC spec, which previously defined `RTCOutboundRTPStreamStats.RTT` instead.
