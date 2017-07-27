---
title: "`IDBObjectStore.getAll` と関連メソッドの接頭辞が外れました"
date: "2015-10-25T21:09:00-07:00"
categories: ["dom"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=920633"
      title: "Bug 920633 - Add getAllKeys to IDBObjectStore"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1196841"
      title: "Bug 1196841 - Add EnforceRange to getAll/getAllKeys to match the spec, and expose them unconditionally"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/De8vLz23Yao/discussion"
      title: "Intent to ship: IDB getAll/getAllKeys/openKeyCursor"
aliases:
    - "/ja/docs/2015/idbobjectstore-getall-and-related-methods-will-be-unprefixed/"
---
Firefox 44 で `IDBObjectStore.mozGetAll`、`IDBIndex.mozGetAll`、`IDBIndex.mozGetAllKeys` の各メソッドから接頭辞が外れました。それらの接頭辞なし版となる `IDBObjectStore.getAll`、`IDBIndex.getAll`、`IDBIndex.getAllKeys` は Firefox 27 で実装され、使うには隠し設定が必要でしたが、この変更により初期設定で有効化されました。
