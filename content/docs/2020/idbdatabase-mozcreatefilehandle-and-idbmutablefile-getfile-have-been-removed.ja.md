---
title: "`IDBDatabase.mozCreateFileHandle()` と `IDBMutableFile.getFile()` が廃止されました"
date: "2020-01-14T21:26:00-05:00"
categories: ["dom"]
tags: []
releases: ["74"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1024312"
      title: "Bug 1024312 - Deprecate mozCreateFileHandle() in favor of createMutableFile()"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1607791"
      title: "Bug 1607791 - Get rid of IDBMutableFile.getFile()"
aliases:
  - "/ja/docs/2020/idbdatabase-mozcreatefilehandle-has-been-removed/"
---
Firefox 74 で、[FileHandle API](https://developer.mozilla.org//docs/Web/API/File_Handle_API) に 2 つの変更が行われました。

[Firefox 33](https://www.fxsitecompat.dev/ja/docs/2014/filehandle-api-has-been-updated/) 以降廃止予定となっていた [`IDBDatabase`](https://developer.mozilla.org/docs/Web/API/IDBDatabase) インターフェイス上の非標準 `mozCreateFileHandle` メソッドが削除されました。標準の `createMutableFile` メソッドで代用してください。

[`IDBMutableFile`](https://developer.mozilla.org/docs/Web/API/IDBMutableFile) インターフェイス上の非標準 `getFile` メソッドが削除されました。他のどのブラウザーも対応していないため、互換性への影響は軽微なはずです。[以前は](https://www.fxsitecompat.dev/ja/docs/2014/filehandle-api-has-been-updated/) `FileHandle` と呼ばれていたインターフェイス自体も近々廃止されます。
