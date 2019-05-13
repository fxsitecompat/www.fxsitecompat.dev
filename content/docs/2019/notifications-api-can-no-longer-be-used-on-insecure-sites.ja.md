---
title: "Notifications API が安全でないサイトでは使用できなくなりました"
date: "2019-05-13T01:47:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["67"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1429432"
      title: "Bug 1429432 - Consider making Notifications require SecureContext"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/FMPrIMGBNtg/discussion"
      title: "Intent to require Secure Context for Web Notifications"
---
Firefox 67 以降、Notifications API でサービスワーカーを通じたプッシュ通知を含むデスクトップ通知の表示許可を要求するためには、サイトを HTTPS で配信する必要があります。Service Worker API と Push API を使用するには常時安全なサイトが必要とされてきたため、この変更は `Notification.requestPermission` メソッドの従来型のユースケースにのみ影響し、これは Mozilla の Telemetry によれば 2% 以下となっています。要求が禁止された場合、コンソールにエラーが記録されます。[Google Chrome](https://www.chromestatus.com/feature/5759967025954816) は既に 62 で同様の変更を行っています。
