---
title: "FileHandle API が更新されました"
date: "2014-07-22T05:06:26-04:00"
categories: ["dom"]
tags: []
versions: ["33"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1006485"
      title: "Bug 1006485 – FileHandle: Rename FileHandle to MutableFile and LockedFile to FileHandle"
---
[FileHandle API](https://developer.mozilla.org/ja/docs/Web/API/File_Handle_API) の実装が更新され、[`IDBDatabase.mozCreateFileHandle`](https://developer.mozilla.org/ja/docs/Web/API/IDBDatabase.mozCreateFileHandle) メソッドは [`IDBDatabase.createMutableFile`](https://developer.mozilla.org/ja/docs/Web/API/IDBDatabase.createMutableFile) に改名されました。また、[`FileHandle`](https://developer.mozilla.org/ja/docs/Web/API/FileHandle)、[`LockedFile`](https://developer.mozilla.org/ja/docs/Web/API/LockedFile) 両インターフェイスはそれぞれ [`IDBMutableFile`](https://developer.mozilla.org/ja/docs/Web/API/IDBMutableFile)、[`IDBFileHandle`](https://developer.mozilla.org/ja/docs/Web/API/IDBFileHandle) へ改名されました。ただし開発者がそれらのオブジェクト名を直接確認する必要はありません。
