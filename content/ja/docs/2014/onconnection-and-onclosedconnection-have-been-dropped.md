---
title: "`onconnection` と `onclosedconnection` が削除されました"
date: "2014-06-09T02:46:54-04:00"
categories: ["webrtc"]
tags: []
versions: "32"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1014304": "Bug 1014304 – Remove onconnection and onclosedconnection from PC"
---
`onconnection`、`onclosedconnection` 両プロパティが、仕様から削除されたため、現在のところ `mozRTCPeerConnection` として実装されている [`RTCPeerConnection`](https://developer.mozilla.org/ja/docs/Web/API/RTCPeerConnection) インタフェースからも削除されました。
