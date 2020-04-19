---
title: "一部の `RTCPeerConnection` メソッドが近々コールバック必須となります"
date: "2014-10-17T22:50:44-04:00"
categories: ["audio-video"]
tags: []
versions: ["35", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1064088"
      title: "Bug 1064088 – PeerConnection should log deprecation warnings when required callbacks are missing."
---
[`RTCPeerConnection`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection) インターフェイス上の [`setLocalDescription`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection.setLocalDescription)、[`setRemoteDescription`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection.setRemoteDescription)、[`addIceCandidate`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection.addIceCandidate) 各メソッドは、成功コールバックとエラーコールバックを引数として取ることができます。更新された仕様に従い、Firefox 32 でこれらのコールバック引数が必須となりましたが、[サイト互換性問題](https://bugzilla.mozilla.org/show_bug.cgi?id=1063971) が報告されたことから、この変更は Firefox 32.0.1 で取り消されました。コールバックは将来的に再び必須となるため、コールバックが与えられていない場合 [ウェブコンソール](https://developer.mozilla.org/docs/Tools/Web_Console) に非推奨であることを知らせる警告が表示されるようになりました。
