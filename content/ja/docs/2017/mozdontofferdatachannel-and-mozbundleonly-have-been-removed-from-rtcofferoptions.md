---
title: "`RTCOfferOptions` から `mozDontOfferDataChannel` と `mozBundleOnly` が削除されました"
date: "2017-07-20T13:08:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["56"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1196974"
      title: "Bug 1196974 - Remove mozDontOfferDataChannel/mozBundleOnly from RTCOfferOptions"
---
非標準で文書化されていない `mozDontOfferDataChannel`、`mozBundleOnly` 両論理属性が `RTCOfferOptions` ディクショナリーから削除されました。これらのオプションは [`RTCPeerConnection.prototype.createOffer`](https://developer.mozilla.org/ja/docs/Web/API/RTCPeerConnection/createOffer) メソッドに使用可能でした。
