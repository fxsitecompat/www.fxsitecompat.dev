---
title: "WebRTC interfaces have been unprefixed"
date: "2015-09-25T02:46:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1155923"
      title: "Bug 1155923 - Unprefix WebRTC"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1206982"
      title: "Bug 1206982 - getUserMedia spec switched from PermissionDeniedError to SecurityError"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/V0A6ZFPYfac/discussion"
      title: "Intent to implement and ship"
---
The [`RTCPeerConnection`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection), [`RTCSessionDescription`](https://developer.mozilla.org/docs/Web/API/RTCSessionDescription) and `RTCIceCandidate` interfaces have been unprefixed. The `navigator.mozGetUserMedia` method has also been deprecated in favour of [`navigator.mediaDevices.getUserMedia`](https://developer.mozilla.org/docs/Web/API/MediaDevices/getUserMedia). The `moz`-prefixed interfaces and method will be removed soon.

Also, the `PermissionDeniedError` error code, passed to the error callback of the `getUserMedia` method when the permission to use a media device is denied, has been renamed to `SecurityError` according to the latest spec.
