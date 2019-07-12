---
title: "`Referer` ヘッダーサイズが 4 KB に制限されました"
date: "2019-07-11T23:03:00-04:00"
categories: ["networking"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1557346"
      title: "Bug 1557346 - Experiment limit `referer` header length"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/GWvDmAn8n3M/discussion"
      title: "Intent to implement and ship: Limit the length of Referer header to 4k"
---
Firefox 70 以降、`Referer` HTTP リクエストヘッダーのサイズが 4 KB (4,096 バイト) に制限されます。極端に長いリファラーが定義された制限を超えた場合、オリジン部分のみが送信されます。実際に起こることは考えづらいものの、オリジン部分がまだ制限を超えている場合、ヘッダーは完全に切り詰められます。

[Google Chrome](https://www.chromestatus.com/feature/5648956820291584) は既に同じ変更をバージョン 77 で行っています。
