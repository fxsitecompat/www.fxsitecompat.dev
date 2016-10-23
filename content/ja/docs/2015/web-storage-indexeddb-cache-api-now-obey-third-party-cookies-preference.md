---
title: "Web Storage、IndexedDB、Cache API がサードパーティ Cookie 設定に従うようになりました"
date: "2015-10-24T16:10:00-07:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["43"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=536509"
      title: "Bug 536509 - localStorage does not obey \"third-party cookies\" pref"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1147821"
      title: "Bug 1147821 - Only disable IndexedDB in third-party windows when the third-party cookie preference is set"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1145744"
      title: "Bug 1145744 - Disallow Cache API in 3rd party windows when 3rd party cookies are disabled"
---
[Web Storage API](https://developer.mozilla.org/ja/docs/Web/API/Web_Storage_API) がブラウザーのサードパーティ Cookie 設定を尊重するようになったため、スクリプトがサードパーティ文脈にあり、ユーザーが [サードパーティ Cookie を無効化している](https://support.mozilla.org/ja/kb/disable-third-party-cookies) 場合は動作しなくなります。[IndexedDB API](https://developer.mozilla.org/ja/docs/Web/API/IndexedDB_API) と新しい [Service Worker Cache API](https://developer.mozilla.org/ja/docs/Web/API/Cache) も同じ制約に従います。
