---
title: "Service Worker が Firefox 45 ESR で無効化されました"
date: "2016-03-07T10:52:00-05:00"
categories: ["dom"]
tags: []
versions: ["45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1232029"
      title: "Bug 1232029 - disable service workers in 45 ESR"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/yuNHtDhl3lY/discussion"
      title: "Intent to disable service workers in 45 ESR"
---
Firefox 44 より使用可能となった [Service Worker API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) が、Firefox 45 [延長サポート版](https://www.mozilla.org/firefox/organizations/) (ESR) で無効化されました。仕様と実装がいずれも 2016 年中に変更される可能性があり、安定した ESR チャンネル上でそのような API を提供するとサイト互換性問題を生む恐れがあるためです。この API は他のチャンネルでは引き続き使用可能です。

**更新**: これらの API は引き続き [Firefox 52 ESR でも無効化されています](https://www.fxsitecompat.dev/ja/docs/2017/service-workers-and-push-notifications-are-disabled-on-firefox-52-esr/).

**更新 2**: これらの API は引き続き [Firefox 60 ESR でも無効化されています](https://www.fxsitecompat.dev/ja/docs/2018/service-workers-and-push-notifications-are-disabled-on-firefox-60-esr/).
