---
title: "Application Cache ストレージが廃止されました"
date: "2020-04-17T08:01:00-04:00"
categories: ["html"]
tags: []
versions: ["77"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1237782"
      title: "Bug 1237782 - Remove support for appcache storage in Nightly and early beta"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1619673"
      title: "Bug 1619673 - Disable appcache in release"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/5JqnS_PnKqU/discussion"
      title: "Intent to unship AppCache"
aliases:
    - "/ja/docs/2016/application-cache-support-will-be-removed/"
    - "/ja/docs/2019/application-cache-storage-has-been-removed-in-nightly-and-early-beta/"
---
[Firefox 44](https://www.fxsitecompat.dev/ja/docs/2015/application-cache-api-has-been-deprecated/) 以降廃止予定となっており、Firefox 71 以降既に Nightly と早期 Beta チャンネルでは廃止されている [HTML Application Cache](https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache) (AppCache) のブラウザーストレージは、Firefox 77 以降すべてのチャンネルで利用できなくなりました。

起こりうるサイトの不具合を防ぐため、`applicationCache` プロパティと `OfflineResourceList` インターフェイスは引き続き `window` 上に露呈されていますが、この何もしなくなった DOM API も近い将来廃止されます。[Service Worker API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) を使って [よりリッチなオフライン体験](https://serviceworke.rs/) を提供しましょう。

Google も [Chrome 84](https://bugs.chromium.org/p/chromium/issues/detail?id=582750#c47) で AppCache ストレージの削除を予定しています。
