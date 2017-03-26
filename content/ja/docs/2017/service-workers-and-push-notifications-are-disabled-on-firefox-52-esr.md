---
title: "Firefox 52 ESR では Service Worker とプッシュ通知が無効化されます"
date: "2017-02-09T16:58:00-05:00"
categories: ["dom"]
tags: []
versions: ["52"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1338144"
      title: "Bug 1338144 - disable service workers and push notifications on 52 ESR"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/TWE4VEbJOmM/discussion"
      title: "Intent to disable service workers and push in 52 ESR"
---
[Service Worker API](https://developer.mozilla.org/ja/docs/Web/API/Service_Worker_API) と [Push API](https://developer.mozilla.org/ja/docs/Web/API/Push_API) は、ブラウザー内での複数のコンテンツプロセスに対応するための大規模な設計変更が予定されていることから、Firefox 52 [延長サポート版](https://www.mozilla.org/ja/firefox/organizations/) (ESR) 上では [Firefox 45 ESR](https://www.fxsitecompat.com/ja/docs/2016/service-workers-have-been-disabled-in-firefox-45-esr/) と同様に無効化されることになりました。Firefox 52 ESR は主に、法人ユーザーと、Firefox 53 以降へアップグレードできない [Windows XP/Vista ユーザー](https://support.mozilla.org/ja/kb/end-support-windows-xp-and-vista) 向けです。これらの API は通常の Release チャンネルでは使用可能です。
