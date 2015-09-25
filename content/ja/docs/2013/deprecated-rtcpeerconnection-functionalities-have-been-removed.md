---
title: "廃止予定となっていた `RTCPeerConnection` の各機能が削除されました"
date: "2013-10-08T20:15:35-04:00"
categories: ["audio-video"]
tags: []
versions: "27"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=929530": "Bug 929530 – Remove deprecated peerConnection functionality which has produced web console warnings since 24."
---
Firefox 24 以降廃止予定となっていたいくつかの非標準機能が (まだ接頭辞付きの) [`RTCPeerConnection`](https://developer.mozilla.org/ja/docs/Web/API/RTCPeerConnection) インタフェースから削除されました。これには、`localStreams`、`remoteStreams`、`readyState`、`onicechange`、`ongatheringchange` 属性と、`failureCallback` を伴わない `createAnswer` や `createOffer` の呼び出しが含まれます。
