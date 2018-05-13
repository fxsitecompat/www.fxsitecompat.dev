---
title: "`RTCPeerConnection.getLocalStreams`, `getRemoteStreams` have been deprecated"
date: "2016-05-25T15:17:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1271669"
      title: "Bug 1271669 - Allow any MediaStream to be passed to RTCPeerConnection.addTrack"
---
The [`RTCPeerConnection.getLocalStreams`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection/getLocalStreams) and [`getRemoteStreams`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection/getRemoteStreams) methods are now considered deprecated due to the removal from the spec. Also, the `addTrack` method now takes any [`MediaStream`](https://developer.mozilla.org/docs/Web/API/MediaStream) that may be returned by `getLocalStreams`. Use the `getSenders` and `getReceivers` methods instead.
