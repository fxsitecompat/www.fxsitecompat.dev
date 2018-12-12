---
title: "`RTCIceCandidateStats.mozLocalTransport` が廃止予定となりました"
date: "2018-10-23T16:20:00-04:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["64"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1435789"
      title: "Bug 1435789 - Deprecate RTCIceCandidateStats.mozLocalTransport and add protocol and relayProtocol"
---
[`RTCPeerConnection.getStats()`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection/getStats) や類似のメソッドによって返される `RTCIceCandidateStats` ディクショナリー上の非標準プロパティ `mozLocalTransport` が廃止予定となり、近い将来削除されることとなりました。標準化された `relayProtocol` プロパティを代わりに使用してください。

**更新**: このプロパティは [Firefox 65](https://www.fxsitecompat.com/ja/docs/2018/rtcicecandidatestats-has-been-updated-to-the-latest-spec/) で廃止されました。
