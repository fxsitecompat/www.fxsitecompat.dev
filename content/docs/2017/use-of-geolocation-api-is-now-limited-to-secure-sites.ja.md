---
title: "Geolocation API の使用が安全なサイトに制限されました"
date: "2017-03-09T14:18:00-05:00"
categories: ["misc", "privacy-security"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1072859"
      title: "Bug 1072859 - Disable Geolocation on non-secure origins"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/wouDQLBbm9A/discussion"
      title: "Intent to ship: Restrict geolocation.watchPosition to secure contexts"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/BvcsTpAqIsQ/discussion"
      title: "Intent to restrict to secure contexts: navigator.geolocation"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/8BsF76gNhDE/discussion"
      title: "Intent to deprecate: insecure Geo requests"
aliases:
    - "/ja/docs/2016/use-of-geolocation-watchposition-will-be-limited-to-secure-sites/"
    - "/ja/docs/2016/use-of-geolocation-api-will-be-limited-to-secure-sites/"
---
現在進行中の [安全でない HTTP 廃止](https://www.fxsitecompat.dev/ja/docs/2015/insecure-http-will-be-deprecated/) の一環として、[`getCurrentPosition`](https://developer.mozilla.org/docs/Web/API/Geolocation/getCurrentPosition)、[`watchPosition`](https://developer.mozilla.org/docs/Web/API/Geolocation/watchPosition) メソッドなどの [Geolocation API](https://developer.mozilla.org/docs/Web/API/Geolocation) は、安全な接続を使用しているサイトのみで使用可能となりました。[Chrome 50](https://developers.google.com/web/updates/2016/04/geolocation-on-secure-contexts-only) が 2016 年 4 月より既にこの制限を導入していることから、現時点での互換性リスクは低いものと思われます。解決策は、言うまでもなく、サイトを HTTPS へ移行することです。
