---
title: "`RTCInboundRTPStreamStats.mozRtt` の接頭辞が外れました"
date: "2017-06-07T08:50:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["55", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1344970"
      title: "Bug 1344970 - Rename mozRtt stat to roundTripTime and change behavior to match spec"
---
[`RTCInboundRTPStreamStats`](https://w3c.github.io/webrtc-stats/#inboundrtpstats-dict*) ディクショナリー上の `mozRtt` プロパティが、最新の WebRTC 仕様に従って `roundTripTime` へ改名されました。仕様では従来その代わりに `RTCOutboundRTPStreamStats.RTT` が定義されていました。
