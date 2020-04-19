---
title: "Firefox 60 ESR では Service Worker とプッシュ通知が無効化されます"
date: "2018-05-06T18:00:00-04:00"
categories: ["dom"]
tags: []
versions: ["60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1457915"
      title: "Bug 1457915 - disable service workers and push notification on 60 ESR"
---
[Service Worker API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) と [Push API](https://developer.mozilla.org/docs/Web/API/Push_API) は、ブラウザー内での複数コンテンツプロセスへ適切に対応するための設計変更が続いていることから、[Firefox 45](https://www.fxsitecompat.dev/ja/docs/2016/service-workers-have-been-disabled-in-firefox-45-esr/)、[Firefox 52](https://www.fxsitecompat.dev/ja/docs/2017/service-workers-and-push-notifications-are-disabled-on-firefox-52-esr/) ESR と同様に Firefox 60 [延長サポート版](https://www.mozilla.org/firefox/organizations/) (ESR) 上でも無効化されることになりました。Firefox ESR は主に大企業や大学内での一括導入向けです。これらの API は通常の Release チャンネルでは使用可能です。
