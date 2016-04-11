---
title: "`RTCStatsReport` has become `Map`-like object"
date: "2016-04-10T23:00:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["48"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1213056"
      title: "Bug 1213056 - Change RTCStatsReport to be maplike."
---
The implementation of [`RTCStatsReport`](https://developer.mozilla.org/en-US/docs/Web/API/RTCStatsReport), that can be retrieved using the `RTCPeerConnection.getStats` method, has been updated as per the latest WebRTC spec, and the interface has become an object like [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map), offering the `entries`, `forEach`, `get`, `has`, `keys`, `values`, `@@iterator` methods as well as the `size` property. The legacy implementation, that allowed to access read-only enumerable properties directly on the object, will be removed soon. As [this example](https://w3c.github.io/webrtc-pc/#example) shows, you basically have to replace `report[key]` with `report.get(key)`.
