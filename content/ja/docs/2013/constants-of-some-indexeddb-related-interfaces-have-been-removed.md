---
title: "一部 IndexedDB 関連インタフェースの定数が削除されました"
date: "2013-07-14T19:12:37-04:00"
categories: ["dom"]
tags: []
versions: ["25"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=887524"
      title: "Bug 887524 – Move IDBRequest to WebIDL"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=888598"
      title: "Bug 888598 – Move IDBTransaction to WebIDL"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=891944"
      title: "Bug 891944 – Move IDBCursor to WebIDL"
---
[`IDBRequest`](https://developer.mozilla.org/ja/docs/Web/API/IDBRequest)、[`IDBTransaction`](https://developer.mozilla.org/ja/docs/Web/API/IDBTransaction)、[`IDBCursor`](https://developer.mozilla.org/ja/docs/Web/API/IDBCursor) 各インタフェースの以下の定数が、仕様の廃止に伴って削除されました。`IDBRequest.LOADING`、`IDBRequest.DONE`、`IDBTransaction.READ_ONLY`、`IDBTransaction.READ_WRITE`、`IDBTransaction.VERSION_CHANGE`、`IDBCursor.NEXT`、`IDBCursor.NEXT_NO_DUPLICATE`、`IDBCursor.PREV`、`IDBCursor.PREV_NO_DUPLICATE`
