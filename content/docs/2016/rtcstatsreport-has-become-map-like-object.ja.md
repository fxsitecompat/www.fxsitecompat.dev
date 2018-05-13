---
title: "`RTCStatsReport` が `Map` のようなオブジェクトになりました"
date: "2016-04-10T23:00:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["48"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1213056"
      title: "Bug 1213056 - Change RTCStatsReport to be maplike."
---
`RTCPeerConnection.getStats` メソッドで取得可能な [`RTCStatsReport`](https://developer.mozilla.org/docs/Web/API/RTCStatsReport) の実装が最新の WebRTC 仕様に合わせて更新され、このインターフェイスは `entries`、`forEach`、`get`、`has`、`keys`、`values`、`@@iterator` メソッドと `size` プロパティを提供する [`Map`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Map) のようなオブジェクトになりました。オブジェクト上で読み取り専用の加算プロパティへ直接アクセス可能な古い実装は、コンソールで警告が表示されるようになり、まもなく削除されます。[この例](https://w3c.github.io/webrtc-pc/#example) が示す通り、要するに `report[key]` を `report.get(key)` に書き換えなくてはなりません。
