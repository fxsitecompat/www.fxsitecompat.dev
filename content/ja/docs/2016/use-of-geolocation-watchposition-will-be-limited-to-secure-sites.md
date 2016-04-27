---
title: "`Geolocation.watchPosition()` の使用が安全なサイトに制限されます"
date: "2016-04-26T22:17:00-04:00"
categories: ["misc", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1072859"
      title: "Bug 1072859 - Deprecate non-TLS usage of geolocation"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1266494"
      title: "Bug 1266494 - Limit navigator.geolocation.watchPosition() to secure contexts"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/wouDQLBbm9A/discussion"
      title: "Intent to ship: Restrict geolocation.watchPosition to secure contexts"
---
[安全でない HTTP 廃止](https://www.fxsitecompat.com/ja/docs/2015/insecure-http-will-be-deprecated/) の一環として、[Geolocation API](https://developer.mozilla.org/ja/docs/Web/API/Geolocation) は安全な接続を使用しているサイトのみで使用可能となります。Chrome 50 は既にこの制限を導入しています。Mozilla 開発者も Firefox 内で安全でないサイトによる [`watchPosition`](https://developer.mozilla.org/ja/docs/Web/API/Geolocation/watchPosition) メソッドの使用を禁止することを検討しています。これは「パワフルな」機能であり、その一方で [`getCurrentPosition`](https://developer.mozilla.org/ja/docs/Web/API/Geolocation/getCurrentPosition) より使用例が少ないことが理由として挙げられています。
