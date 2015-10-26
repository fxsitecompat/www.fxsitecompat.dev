---
title: "`IDBObjectStore.getAll` と関連メソッドの接頭辞が外れます"
date: "2015-10-25T21:09:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=920633": "Bug 920633 - Add getAllKeys to IDBObjectStore"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1196841": "Bug 1196841 - Add EnforceRange to getAll/getAllKeys to match the spec, and expose them unconditionally"
    "https://groups.google.com/d/topic/mozilla.dev.platform/De8vLz23Yao/discussion": "Intent to ship: IDB getAll/getAllKeys/openKeyCursor"
---
近い将来 `IDBObjectStore.mozGetAll`、`IDBIndex.mozGetAll`、`IDBIndex.mozGetAllKeys` の各メソッドから接頭辞が外れることになりました。それらの接頭辞なし版となる `IDBObjectStore.getAll`、`IDBIndex.getAll`、`IDBIndex.getAllKeys` は実際のところ Firefox 27 で実装されましたが、初期設定で無効化されています。
