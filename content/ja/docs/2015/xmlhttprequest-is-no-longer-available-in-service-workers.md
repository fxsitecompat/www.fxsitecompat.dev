---
title: "`XMLHttpRequest` は Service Worker 内で使用できなくなりました"
date: "2015-10-23T01:34:00-07:00"
categories: ["dom"]
tags: []
versions: ["44"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=931243": "Bug 931243 - XMLHttpRequest should be disabled on ServiceWorkers"
---
[`XMLHttpRequest`](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest) API が、最新の仕様に従い [Service Worker](https://developer.mozilla.org/ja/docs/Web/API/Service_Worker_API) 内で無効化されました。Service Worker API は今のところ [Developer Edition](https://www.mozilla.org/ja/firefox/developer/) (Aurora) と Nightly チャンネルでのみ有効化されているため、互換性への影響は限定的です。
