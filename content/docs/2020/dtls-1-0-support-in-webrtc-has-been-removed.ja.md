---
title: "WebRTC の DTLS 1.0 対応が廃止されました"
date: "2020-02-19T20:27:00-05:00"
categories: ["audio-video", "networking", "privacy-security"]
tags: []
versions: ["75"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1615445"
      title: "Bug 1615445 - Set minimum DTLS version to 1.2"
    - url: "https://blog.mozilla.org/webrtc/removing-old-versions-of-dtls/"
      title: "Removing Old Versions of DTLS - Advancing WebRTC"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/wUoBf0FqqcE/discussion"
      title: "Intent to unship: DTLS 1.0 for WebRTC"
---
Firefox 75 で WebRTC における [Datagram Transport Layer Security](https://developer.mozilla.org/docs/Glossary/DTLS) (DTLS) の既定最小バージョンが 1.2 に引き上げられました。Mozilla によれば、98% 以上の WebRTC サービスが既に DTLS 1.2 を採用しています。もしまだ DTLS 1.0 を使用している場合は、今がアップグレードの時期です。
