---
title: "WebRTC の DTLS 1.0 対応が廃止されました"
date: "2020-02-19T20:27:00-05:00"
categories: ["audio-video", "networking", "privacy-security"]
tags: []
versions: ["75"]
statuses: "postponed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1615445"
      title: "Bug 1615445 - Set minimum DTLS version to 1.2"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1623511"
      title: "Bug 1623511 - Turn DTLS 1.0 back on to prevent sites breaking during Covid-19 traffic increase"
    - url: "https://blog.mozilla.org/webrtc/removing-old-versions-of-dtls/"
      title: "Removing Old Versions of DTLS - Advancing WebRTC"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/wUoBf0FqqcE/discussion"
      title: "Intent to unship: DTLS 1.0 for WebRTC"
---
Firefox 75 で WebRTC における [Datagram Transport Layer Security](https://developer.mozilla.org/docs/Glossary/DTLS) (DTLS) の既定最小バージョンが 1.2 に引き上げられました。Mozilla によれば、98% 以上の WebRTC サービスが既に DTLS 1.2 を採用しています。もしまだ DTLS 1.0 を使用している場合は、今がアップグレードの時期です。

**更新**: Mozilla は Firefox 75 Beta の DTLS 1.0 対応を一時的に再有効化する方針です。これは、新型コロナウイルス (COVID-19) の流行を受けて、現在多くの人が在宅勤務を強いられビデオ会議ソリューションに依存していますが、そうしたサービスのひとつである *Jitsi* がまだ DTLS 1.2 に対応していないためです。また COVID-19 を理由として、Google が [DTLS 1.0 対応を廃止](https://bugs.chromium.org/p/webrtc/issues/detail?id=10261) する予定となっていた [Chrome 82 の公開を延期](https://blog.chromium.org/2020/03/upcoming-chrome-releases.html) しています。状況が変わり次第このドキュメントを更新します。
