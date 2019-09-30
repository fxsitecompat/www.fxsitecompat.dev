---
title: "Application Cache ストレージが Nightly と早期ベータ版から削除されました"
date: "2019-09-30T17:08:00-04:00"
categories: ["html"]
tags: []
versions: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1237782"
      title: "Bug 1237782 - Remove support for appcache storage in Nightly and early beta"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/5JqnS_PnKqU/discussion"
      title: "Intent to unship AppCache"
---
[Firefox 44](https://www.fxsitecompat.dev/ja/docs/2015/application-cache-api-has-been-deprecated/) 以降廃止予定となっていた HTML5 Application Cache (AppCache) のブラウザーストレージは、Firefox 71 以降の Nightly と早期 Beta/DevEdition チャンネルでは使用できなくなりました。数リリース後にすべてのチャンネルから削除されます。`applicationCache` プロパティと `OfflineResourceList` インターフェイスは引き続き `window` 上に露呈されていますが、この API も近い将来廃止されます。代わりに [Service Worker API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) を使用してください。
