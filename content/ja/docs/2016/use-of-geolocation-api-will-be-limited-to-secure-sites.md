---
title: "Geolocation API の使用が安全なサイトに制限されます"
date: "2016-04-26T22:17:00-04:00"
categories: ["misc", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1072859"
      title: "Bug 1072859 - Disable Geolocation on non-secure origins"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/wouDQLBbm9A/discussion"
      title: "Intent to ship: Restrict geolocation.watchPosition to secure contexts"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/BvcsTpAqIsQ/discussion"
      title: "Intent to restrict to secure contexts: navigator.geolocation"
aliases:
    - "/docs/2016/use-of-geolocation-watchposition-will-be-limited-to-secure-sites/"
---
[安全でない HTTP 廃止](https://www.fxsitecompat.com/ja/docs/2015/insecure-http-will-be-deprecated/) の一環として、[Geolocation API](https://developer.mozilla.org/ja/docs/Web/API/Geolocation) はまもなく安全な接続を使用しているサイトのみで使用可能となります。[Chrome 50](https://developers.google.com/web/updates/2016/04/geolocation-on-secure-contexts-only) は既にこの制限を導入しています。

**更新**: Mozilla 開発者が [`watchPosition`](https://developer.mozilla.org/ja/docs/Web/API/Geolocation/watchPosition) だけでなく [`getCurrentPosition`](https://developer.mozilla.org/ja/docs/Web/API/Geolocation/getCurrentPosition) メソッドも安全でないサイト上で無効化する決定を下したことから、このドキュメントを更新しました。
