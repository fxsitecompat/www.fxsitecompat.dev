---
title: "`KeyboardEvent.key` の値が最新仕様に合わせて更新されました"
date: "2015-01-16T09:37:54-05:00"
categories: ["dom"]
tags: []
versions: ["37"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=900372"
      title: "Bug 900372 – Update key names for the latest D3E draft"
---
[`KeyboardEvent.key`](https://developer.mozilla.org/docs/Web/API/KeyboardEvent/key) プロパティによって返される一部のキー値が、最新の DOM Level 3 Events 仕様に合わせて更新されました。これには、[Firefox 33 以降廃止予定となっていた](https://www.fxsitecompat.com/ja/docs/2014/some-keyboardevent-key-values-have-been-deprecated/) `Left`、`Right`、`Del`、`Esc` が含まれます。変更点に関しては [Bug 900372 の依存バグ](https://bugzilla.mozilla.org/showdependencytree.cgi?id=900372&maxdepth=1&hide_resolved=0) を、取り得るすべての値の一覧は [`KeyboardEvent.key`](https://developer.mozilla.org/docs/Web/API/KeyboardEvent/key) のドキュメントを参照してください。
