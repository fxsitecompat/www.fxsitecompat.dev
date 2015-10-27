---
title: "安全でない HTTP は廃止予定となります"
date: "2015-10-27T16:00:00-07:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["future"]
statuses: "affected"
references:
    "https://groups.google.com/d/topic/mozilla.dev.platform/GDSnSI9inOo/discussion": "Deprecate geolocation and getUserMedia() for unauthenticated origins"
    "https://groups.google.com/d/topic/mozilla.dev.platform/vavZdN4tX44/discussion": "Intent to deprecate: persistent permissions over HTTP"
    "https://groups.google.com/d/topic/mozilla.dev.platform/xaGffxAM-hs/discussion": "Intent to deprecate: Insecure HTTP"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1072859": "Bug 1072859 - Deprecate non-TLS usage of geolocation"
---

インターネット接続は常に暗号化されるべきという提案に関して、業界は大筋で合意に達しています。Mozilla 開発者の提案によれば、[Geolocation](https://developer.mozilla.org/ja/docs/Web/API/Geolocation/Using_geolocation)、[Notification](https://developer.mozilla.org/ja/docs/Web/API/Notifications_API)、[Fullscreen](https://developer.mozilla.org/ja/docs/Web/API/Fullscreen_API)、[Pointer Lock](https://developer.mozilla.org/ja/docs/Web/API/Pointer_Lock_API)、[Media Stream](https://developer.mozilla.org/ja/docs/Web/API/Media_Streams_API) API といったユーザの許可設定を必要する一部の機能に関して、まず HTTPS が必須となる可能性があります。

まだ明確なスケジュールは出されていませんが、安全でない HTTP の廃止はそう遠くない将来に行われます。Web コンテンツ提供者にはできる限り早い時期に HTTPS への移行計画を立てるよう強く推奨します。移行を容易にするため、Mozilla などが運営する新しい認証局 [Let's Encrypt](https://letsencrypt.org/) が、2015 年 11 月以降、信頼の置ける証明書を誰にでも無償で提供します。

このドキュメントは最新の状況に基づいて更新します。
