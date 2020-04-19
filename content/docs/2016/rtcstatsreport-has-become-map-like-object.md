---
title: "`RTCStatsReport` has become `Map`-like object"
date: "2016-04-10T23:00:00-04:00"
categories: ["audio-video"]
tags: []
releases: ["48", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1213056"
      title: "Bug 1213056 - Change RTCStatsReport to be maplike."
---
The implementation of [`RTCStatsReport`](https://developer.mozilla.org/docs/Web/API/RTCStatsReport), that can be retrieved using the `RTCPeerConnection.getStats` method, has been updated as per the latest WebRTC spec, and the interface has become an object like [`Map`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Map), offering the `entries`, `forEach`, `get`, `has`, `keys`, `values`, `@@iterator` methods as well as the `size` property. The legacy implementation, that allowed to access read-only enumerable properties directly on the object, will be warned in the Web Console and soon be removed. As [this example](https://w3c.github.io/webrtc-pc/#example) shows, you basically have to replace `report[key]` with `report.get(key)`.

**Update**: The legacy non-`Map`-like `getStats` access has been [removed with Firefox 66](https://www.fxsitecompat.dev/en-CA/docs/2018/legacy-peerconnection-getstats-support-has-been-removed/).
