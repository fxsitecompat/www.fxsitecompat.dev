---
title: "WebRTC における DHE 暗号スイート対応が廃止されました"
date: "2018-10-27T01:09:00-04:00"
categories: ["audio-video", "privacy-security"]
tags: []
versions: ["65"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1227519"
      title: "Bug 1227519 - Establish deprecation date for DHE cipher suites in WebRTC"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/5n16ltyShIE/discussion"
      title: "Intent to remove DHE ciphers in Fx 64 (Was: Intent to remove DHE ciphers from WebRTC DTLS handshake)"
---
以下の DHE 暗号スイート対応が WebRTC Datagram Transport Layer Security (DTLS) ハンドシェイクから削除されました。これらのプロトコルは弱すぎると考えられているためです。Mozilla の Telemetry によれば現時点での DHE の仕様はごくわずかであることから、廃止の互換性リスクは非常に低いはずです。

* `TLS_DHE_RSA_WITH_AES_128_CBC_SHA`
* `TLS_DHE_RSA_WITH_AES_256_CBC_SHA`
