---
title: "Legacy `RTCPeerConnection.getStats()` support has been removed"
date: "2018-12-25T01:19:00-05:00"
categories: ["audio-video"]
tags: []
releases: ["66", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1328194"
      title: "Bug 1328194 - Remove legacy PeerConnection.getStats and associated legacy stats type"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1380555"
      title: "Bug 1380555 - Refactor RTCInboundRTPStreamStats & RTCOutboundRTPStreamStats to catch up with the spec"
aliases:
    - "/en-CA/docs/2018/legacy-peerconnection-getstats-support-has-been-removed/"
---
The implementation of the [`RTCPeerConnection.prototype.getStats`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection/getStats) method has been updated to the current spec with Firefox 66. The changes include:

* The method's callback support, deprecated since [Firefox 53](https://www.fxsitecompat.dev/en-CA/docs/2017/callback-based-rtcpeerconnection-getstats-has-been-deprecated/), has been removed in favour of an [`RTCStatsReport`](https://developer.mozilla.org/docs/Web/API/RTCStatsReport) object returned in `Promise`.
* The legacy dictionary-like `RTCStatsReport` interface access, deprecated since [Firefox 48](https://www.fxsitecompat.dev/en-CA/docs/2016/rtcstatsreport-has-become-map-like-object/), has been removed in favour of the `Map`-like results.
* The `isRemote` property on the `RTCStatsReport` object, deprecated since [Firefox 63](https://www.fxsitecompat.dev/en-CA/docs/2018/rtcrtpstreamstats-isremote-has-been-deprecated/), has been removed in favour of the `remoteId` property.

See the [Advancing WebRTC blog](https://blog.mozilla.org/webrtc/getstats-isremote-66/) for details and examples.
