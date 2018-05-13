---
title: "`indexedDB.open()` の `storage` オプションが廃止予定となりました"
date: "2018-03-07T22:16:00-05:00"
categories: ["dom"]
tags: []
versions: ["60"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1442560"
      title: "Bug 1442560 - Warn about deprecation of storage: persistent"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/3b700_oeAzo/discussion"
      title: "Intent to unship: \"storage\" attribute in options for indexedDB.open()"
---
Firefox 26 以降提供されていた [`indexedDB.open`](https://developer.mozilla.org/docs/Web/API/IDBFactory/open) メソッドの非標準 `storage` オプションが廃止予定と見なされ、Firefox 62 で削除される見通しとなりました。標準化された Storage API の [`navigator.storage.persist`](https://developer.mozilla.org/docs/Web/API/StorageManager/persist) メソッドで代用してください。このオプションは Firefox にしか実装されていないことから、互換性リスクは非常に低いはずです。
