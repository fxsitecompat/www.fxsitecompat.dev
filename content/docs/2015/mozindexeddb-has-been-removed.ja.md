---
title: "`mozIndexedDB` が削除されました"
date: "2015-02-27T04:21:22-05:00"
categories: ["dom"]
tags: []
versions: ["38"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=975699"
      title: "Bug 975699 – Remove mozIndexedDB again"
---
[互換性](https://bugzilla.mozilla.org/show_bug.cgi?id=770844) のために残されていた `mozIndexedDB` プロパティがついに `window` から削除されました。今後は標準の [`indexedDB`](https://developer.mozilla.org/ja/docs/Web/API/IDBEnvironment/indexedDB) プロパティを使用してください。
