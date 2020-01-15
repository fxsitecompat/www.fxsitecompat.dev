---
title: "`IDBDatabase.mozCreateFileHandle()` が廃止されました"
date: "2020-01-14T21:26:00-05:00"
categories: ["dom"]
tags: []
versions: ["74"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1024312"
      title: "Bug 1024312 - Deprecate mozCreateFileHandle() in favor of createMutableFile()"
---
[Firefox 33](https://www.fxsitecompat.dev/ja/docs/2014/filehandle-api-has-been-updated/) 以降廃止予定となっていた [`IDBDatabase`](https://developer.mozilla.org/docs/Web/API/IDBDatabase) インターフェイス上の非標準 `mozCreateFileHandle` メソッドが Firefox 74 で削除されました。標準の `createMutableFile` メソッドで代用してください。
