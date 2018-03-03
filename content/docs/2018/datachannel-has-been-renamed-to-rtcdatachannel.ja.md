---
title: "`DataChannel` が `RTCDataChannel` へ改名されました"
date: "2018-03-03T11:46:00-05:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["60"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1173851"
      title: "Bug 1173851 - Rename DataChannel to RTCDataChannel per specification"
---
これまで Firefox は [`RTCDataChannel`](https://developer.mozilla.org/ja/docs/Web/API/RTCDataChannel) インターフェイスを `DataChannel` として実装しており、これを用いた WebRTC 機能判別に失敗する可能性がありました。仕様に準拠するため、この間違った名称は Firefox 60 で修正されました。Chrome と Safari はいずれも正しい名称でインターフェイスを実装していることから、互換性リスクは低いはずです。
