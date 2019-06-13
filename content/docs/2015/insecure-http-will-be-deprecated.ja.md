---
title: "安全でない HTTP は廃止予定となります"
date: "2015-10-27T16:00:00-07:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["future"]
statuses: "affecting"
references:
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/GDSnSI9inOo/discussion"
      title: "Deprecate geolocation and getUserMedia() for unauthenticated origins"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vavZdN4tX44/discussion"
      title: "Intent to deprecate: persistent permissions over HTTP"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/xaGffxAM-hs/discussion"
      title: "Intent to deprecate: Insecure HTTP"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1072859"
      title: "Bug 1072859 - Disable Geolocation on non-secure origins"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1160368"
      title: "Bug 1160368 - Treat cookies set over non-secure HTTP as session cookies"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1335740"
      title: "Bug 1335740 - Consider disabling getUserMedia on non-secure origins"
    - url: "https://blog.mozilla.org/security/2018/01/15/secure-contexts-everywhere/"
      title: "Mozilla Security Blog: Secure Contexts Everywhere"
---
インターネット接続は常に暗号化されるべきという提案に関して、業界は大筋で合意に達しています。新しい [Service Worker API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) は元々 HTTPS が必須となっています。Mozilla 開発者の提案によれば、[Geolocation](https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation)、[Notification](https://developer.mozilla.org/docs/Web/API/Notifications_API)、[Fullscreen](https://developer.mozilla.org/docs/Web/API/Fullscreen_API)、[Pointer Lock](https://developer.mozilla.org/docs/Web/API/Pointer_Lock_API)、[Media Stream](https://developer.mozilla.org/docs/Web/API/Media_Streams_API) API といったユーザーの許可設定を必要とする一部の機能に関しても、今後 HTTPS が必須となる可能性があります。

また、非 HTTPS の Cookie をセッション Cookie として扱うことで、広告ネットワークとパブリッシャーの HTTPS 移行を促すことも提案されています。

まだ明確なスケジュールは出されていませんが、安全でない HTTP の廃止はそう遠くない将来に行われます。ウェブコンテンツ提供者にはできる限り早い時期に HTTPS への移行計画を立てるよう強く推奨します。移行を容易にするため、Mozilla などが運営する新しい認証局 [Let's Encrypt](https://letsencrypt.org/) が、2015 年 11 月以降、信頼の置ける証明書を誰にでも無償で提供します。

このドキュメントは最新の状況に基づいて更新します。

**更新**: [Firefox 55](https://www.fxsitecompat.dev/ja/docs/2017/use-of-geolocation-api-is-now-limited-to-secure-sites/) 以降、Geolocation API の使用が安全なサイトに制限されました。

**更新 2**: Mozilla は、すべての新機能や一部既存機能について [HTTPS を必須とする](https://blog.mozilla.org/security/2018/01/15/secure-contexts-everywhere/) 方針を 2018 年 1 月に発表しました。[Firefox 60](https://www.fxsitecompat.dev/ja/docs/2017/webvr-can-no-longer-be-used-on-insecure-sites/) 以降、WebVR が安全でないサイト上では使用できなくなりました。
