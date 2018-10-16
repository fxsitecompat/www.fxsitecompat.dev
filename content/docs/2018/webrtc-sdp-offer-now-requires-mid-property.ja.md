---
title: "WebRTC SDP オファーに `mid` プロパティが必須となりました"
date: "2018-10-16T10:12:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["63"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1483338"
      title: "Bug 1483338 - Key media transports by a string id rather than level"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1487617"
      title: "Bug 1487617 - Google Meet and Hangouts stopped working in Firefox 63"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1495569"
      title: "Bug 1495569 - Firefox 63 bricks TextNow.com calls"
---
現在進行中の WebRTC 仕様準拠作業の一環として、Firefox 63 以降、整数レベル ([m-line index](https://developer.mozilla.org/docs/Web/API/RTCIceCandidate/sdpMLineIndex)) の代わりに文字列 ID ([MID](https://developer.mozilla.org/docs/Web/API/RTCIceCandidate/sdpMid)) がメディアトランスポートの識別子として用いられます。このため、SDP オファーも仕様に準拠している必要があり、`mid` プロパティが要求されます。Mozilla エンジニアの [バグコメント](https://bugzilla.mozilla.org/show_bug.cgi?id=1495569#c17) によれば、最も簡単な解決策はオファーに `a=mid:0` を追加することです。

この変更が行われた後 *Google Meet* と *Hangouts* が動作しなくなりましたが、Google は既に問題を修正しています。*TextNow* も動作しないことが判明しています。
