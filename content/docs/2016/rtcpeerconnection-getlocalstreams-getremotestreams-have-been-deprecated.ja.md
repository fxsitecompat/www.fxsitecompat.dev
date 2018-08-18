---
title: "`RTCPeerConnection.getLocalStreams()`、`getRemoteStreams()` が廃止予定となりました"
date: "2016-05-25T15:17:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1271669"
      title: "Bug 1271669 - Allow any MediaStream to be passed to RTCPeerConnection.addTrack"
---
[`RTCPeerConnection.getLocalStreams`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection/getLocalStreams)、[`getRemoteStreams`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection/getRemoteStreams) 両メソッドが、仕様から削除されたため、廃止予定となりました。また、`addTrack` メソッドはあらゆる [`MediaStream`](https://developer.mozilla.org/docs/Web/API/MediaStream) を受け入れるようになり、それが `getLocalStreams` によって返される可能性があります。代わりに `getSenders`、`getReceivers` 両メソッドを使ってください。
