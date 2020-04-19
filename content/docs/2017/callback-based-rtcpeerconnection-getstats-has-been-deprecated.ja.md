---
title: "コールバックベースの `RTCPeerConnection.getStats()` が廃止予定となりました"
date: "2017-03-11T21:04:00-05:00"
categories: ["audio-video"]
tags: []
releases: ["53", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1323095"
      title: "Bug 1323095 - Add deprecation warnings to callback-based pc.getStats()"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1329762"
      title: "Bug 1329762 - Strengthen deprecation warning of legacy PeerConnection.getStats"
---
[`RTCStatsReport`](https://developer.mozilla.org/docs/Web/API/RTCStatsReport) を提供するコールバックベースの `RTCPeerConnection.prototype.getStats` メソッドは、WebRTC 仕様から削除され、Firefox からも近い将来削除されます。Firefox 53 以降のウェブコンソールでは、この旧バージョンに対して廃止予定の警告が表示されます。代わりに新しい [Promise バージョン](https://w3c.github.io/webrtc-pc/#getstats-example) を使用してください。

**更新**: コールバックベースの `getStats` メソッドは [Firefox 66 で削除されました](https://www.fxsitecompat.dev/ja/docs/2018/legacy-peerconnection-getstats-support-has-been-removed/).
