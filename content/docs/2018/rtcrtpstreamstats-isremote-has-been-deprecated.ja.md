---
title: "`RTCRTPStreamStats.isRemote` が廃止予定となりました"
date: "2018-08-14T20:27:00-04:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1393306"
      title: "Bug 1393306 - Add deprecation warning for removal of stat.isRemote in 65."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/kqlQzADXbng/discussion"
      title: "Intent to remove: isRemote member in WebRTC getStats() results"
---
`RTCPeerConnection.prototype.getStats` メソッドがリモート統計用に返す `RTCRTPStreamStats` ディクショナリーの `isRemote` 真偽値メンバーが廃止予定とされ、Firefox 65 で削除されることとなりました。[WebRTC チームのブログ記事](https://blog.mozilla.org/webrtc/getstats-isremote-65/) で説明されている通り、代わりに `remoteId` を使用してください。

**更新**: `isRemote` は [Firefox 66 で削除されました](https://www.fxsitecompat.dev/ja/docs/2018/legacy-peerconnection-getstats-support-has-been-removed/)。
