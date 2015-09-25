---
title: "WebRTC インタフェースの接頭辞が外れました"
date: "2015-09-25T02:46:00-04:00"
categories: ["audio-video"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1155923": "Bug 1155923 - Unprefix WebRTC"
---
[`RTCPeerConnection`](https://developer.mozilla.org/en-US/docs/Web/API/RTCPeerConnection)、[`RTCSessionDescription`](https://developer.mozilla.org/en-US/docs/Web/API/RTCSessionDescription)、`RTCIceCandidate` インタフェースの接頭辞が外れました。`navigator.mozGetUserMedia` メソッドも [`navigator.mediaDevices.getUserMedia`](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getUserMedia) に置き換えられる形で廃止予定となりました。`moz` 接頭辞付きのインタフェースとメソッドは近く削除されます。
