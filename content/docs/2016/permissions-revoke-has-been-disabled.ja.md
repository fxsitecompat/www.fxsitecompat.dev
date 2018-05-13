---
title: "`Permissions.revoke()` が無効化されました"
date: "2016-08-17T13:50:00-04:00"
categories: ["dom"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1295877"
      title: "Bug 1295877 - Put Permissions API .revoke() behind a pref"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/x6XgGCoXUw0/discussion"
      title: "Intent to put Permission API's .revoke() method behind a pref"
---
[Permissions API](https://developer.mozilla.org/docs/Web/API/Permissions_API) の [`Permissions.revoke`](https://developer.mozilla.org/docs/Web/API/Permissions/revoke) メソッドが初期設定で無効化されました。現時点で仕様が安定していないにも関わらず、Firefox 47 で早まって実装されてしまったためです。標準化作業の進捗に応じて、いずれは再度有効化もしくは削除されます。
