---
title: "`indexedDB.open()` の `storage` オプションが廃止されました"
date: "2018-06-03T23:20:00-04:00"
categories: ["dom"]
tags: []
versions: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1354500"
      title: "Bug 1354500 - Remove the proprietary persistent indexedDB permission"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1451486"
      title: "Bug 1451486 - Add a pref for ignoring the storage attribute for indexedDB.open()"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/3b700_oeAzo/discussion"
      title: "Intent to unship: \"storage\" attribute in options for indexedDB.open()"
---
[Firefox 60 以降廃止予定](https://www.fxsitecompat.dev/ja/docs/2018/storage-option-for-indexeddb-open-has-been-deprecated/) となっていた [`indexedDB.open`](https://developer.mozilla.org/docs/Web/API/IDBFactory/open) メソッドの非標準 `storage` オプションが Firefox 61 で初期設定無効となりました。標準化された Storage API の [`navigator.storage.persist`](https://developer.mozilla.org/docs/Web/API/StorageManager/persist) メソッドで代用してください。このオプションは Firefox にしか実装されていないことから、互換性リスクは非常に低いはずです。
