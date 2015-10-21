---
title: "要素の `id` 変更後、変更前の `id` ではアクセスできなくなります"
date: "2013-09-19T23:58:13-04:00"
categories: ["dom"]
tags: []
versions: ["26"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=790601": "Bug 790601 – Javascript element should not exist with old id"
---
`id` 付きの要素は `window.id` DOM オブジェクトとしてアクセス可能です。従来、そうしたオブジェクトは要素の `id` が動的に変更された後も [`window`](https://developer.mozilla.org/ja/docs/Web/API/window) 上に残っていました。この不可解な挙動が Firefox 26 で修正されました。一般的に使用が推奨される [`document.getElementById`](https://developer.mozilla.org/ja/docs/Web/API/document.getElementById) メソッドは、この変更による影響を受けません。
