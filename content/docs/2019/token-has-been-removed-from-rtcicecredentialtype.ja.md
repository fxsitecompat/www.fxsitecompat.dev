---
title: "`RTCIceCredentialType` から `token` が削除されました"
date: "2019-06-09T05:25:00-04:00"
categories: ["audio-video"]
tags: []
releases: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1529595"
      title: "Bug 1529595 - Remove \"token\" from RTCIceCredentialType"
---
現行の WebRTC 1.0 仕様に従い、[`RTCIceServer.prototype.credentialType`](https://developer.mozilla.org/docs/Web/API/RTCIceServer/credentialType) プロパティに用いられる `RTCIceCredentialType` enum から `token` 定数が削除されました。Firefox はまだ仕様に追加された `oauth` に対応していないため、現時点では `password` のみ使用可能となっています。
