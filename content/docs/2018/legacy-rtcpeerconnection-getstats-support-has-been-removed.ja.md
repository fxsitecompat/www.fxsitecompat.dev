---
title: "旧式 `RTCPeerConnection.getStats()` 対応が廃止されました"
date: "2018-12-25T01:19:00-05:00"
categories: ["audio-video"]
tags: []
releases: ["66", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1328194"
      title: "Bug 1328194 - Remove legacy PeerConnection.getStats and associated legacy stats type"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1380555"
      title: "Bug 1380555 - Refactor RTCInboundRTPStreamStats & RTCOutboundRTPStreamStats to catch up with the spec"
aliases:
    - "/ja/docs/2018/legacy-peerconnection-getstats-support-has-been-removed/"
---
[`RTCPeerConnection.prototype.getStats`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection/getStats) メソッドの実装が Firefox 66 で現在の仕様に合わせて更新されました。変更点は以下の通りです。

* [Firefox 53](https://www.fxsitecompat.dev/ja/docs/2017/callback-based-rtcpeerconnection-getstats-has-been-deprecated/) 以降廃止予定となっていたメソッドのコールバック対応が、`Promise` で返される [`RTCStatsReport`](https://developer.mozilla.org/docs/Web/API/RTCStatsReport) オブジェクトに置き換えられる形で廃止されました。
* [Firefox 48](https://www.fxsitecompat.dev/ja/docs/2016/rtcstatsreport-has-become-map-like-object/) 以降廃止予定となっていたディクショナリー形式の `RTCStatsReport` インターフェイスアクセスが、`Map` 形式の結果に置き換えられる形で廃止されました。
* [Firefox 63](https://www.fxsitecompat.dev/ja/docs/2018/rtcrtpstreamstats-isremote-has-been-deprecated/) 以降廃止予定となっていた `RTCStatsReport` オブジェクト上の `isRemote` プロパティが、`remoteId` に置き換えられる形で廃止されました。

詳細と例は [Advancing WebRTC ブログ](https://blog.mozilla.org/webrtc/getstats-isremote-66/) を参照してください。
