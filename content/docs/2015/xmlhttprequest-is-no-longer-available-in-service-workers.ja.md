---
title: "`XMLHttpRequest` は Service Worker 内で使用できなくなりました"
date: "2015-10-23T01:34:00-07:00"
categories: ["dom"]
tags: []
versions: ["44", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=931243"
      title: "Bug 931243 - XMLHttpRequest should be disabled on ServiceWorkers"
---
[`XMLHttpRequest`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest) API が、最新の仕様に従い [Service Worker](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) 内で無効化されました。代わりに [Fetch API](https://developer.mozilla.org/docs/Web/API/Fetch_API) を使ってください。Service Worker API は今のところ [Developer Edition](https://www.mozilla.org/firefox/developer/) (Aurora) と Nightly チャンネルでのみ有効化されているため、互換性への影響は限定的です。

**更新**: Service Worker API は Firefox 44 で正式公開となり、Beta、Release 両チャンネルでも利用可能となりました。
