---
title: "`RTCPeerConnection.removeStream()` が削除されました"
date: "2016-08-08T08:23:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["51", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1213441"
      title: "Bug 1213441 - Remove RTCPeerConnection.removeStream for good."
---
廃止予定となっていた [`RTCPeerConnection.removeStream`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection/removeStream) メソッドが Firefox 51 で廃止されました。仕様変更により、これは実際のところ Firefox 22 以降 `NotSupportedError` 例外を投げていました。[`removeTrack`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection/removeTrack) メソッドを代用してください。
