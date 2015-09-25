---
title: "WebRTC interfaces have been unprefixed"
date: "2015-09-25T02:46:00-04:00"
categories: ["audio-video"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1155923": "Bug 1155923 - Unprefix WebRTC"
---
The [`RTCPeerConnection`](https://developer.mozilla.org/en-US/docs/Web/API/RTCPeerConnection), [`RTCSessionDescription`](https://developer.mozilla.org/en-US/docs/Web/API/RTCSessionDescription) and `RTCIceCandidate` interfaces have been unprefixed. The `navigator.mozGetUserMedia` method has also been deprecated in favor of [`navigator.mediaDevices.getUserMedia`](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getUserMedia). The `moz`-prefixed interfaces and method will be removed soon.
