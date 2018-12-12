---
title: "`RTCIceCandidateStats` が最新の仕様に合わせて更新されました"
date: "2018-12-12T08:22:00-05:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["65"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1324788"
      title: "Bug 1324788 - Update RTCIceCandidateStats to spec"
---
`RTCIceCandidateStats` ディクショナリーの実装が現行の WebRTC 仕様に合わせて更新されました。後方互換性のない変更は以下の通りです。

* 廃止予定となっていた `candidateId` プロパティが削除されました。
* `candidateType` enum メンバーが改名されました。`serverreflexive`、`peerreflexive` と `relayed` はそれぞれ `srflx`、`prflx` と `relay` になりました。
* `componentId` プロパティが削除されました。標準化された `transportId` プロパティはまだ Firefox では使えません。
* [廃止予定となっていた](https://www.fxsitecompat.com/ja/docs/2018/rtcicecandidatestats-mozlocaltransport-has-been-deprecated/) `mozLocalTransport` プロパティが `relayProtocol` へ改名されました。
* `portNumber` プロパティが `port` へ改名されました。
* `transport` プロパティが `protocol` へ改名されました。
