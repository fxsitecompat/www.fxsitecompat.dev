---
title: "`RTCPeerConnection.removeStream()` has been removed"
date: "2016-08-08T08:23:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["51", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1213441"
      title: "Bug 1213441 - Remove RTCPeerConnection.removeStream for good."
---
The deprecated [`RTCPeerConnection.removeStream`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection/removeStream) method has been dropped from Firefox 51. It was actually raising a `NotSupportedError` exception since Firefox 22 because of the spec change. Use the [`removeTrack`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection/removeTrack) method instead.
