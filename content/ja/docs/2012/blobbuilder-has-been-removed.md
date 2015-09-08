---
title: "`BlobBuilder` が廃止されました"
date: "2012-12-03T03:53:26-05:00"
categories: ["dom"]
tags: []
versions: "18"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=744907": "Bug 744907 – Remove BlobBuilder"
---
廃止予定となっていた [`BlobBuilder`](https://developer.mozilla.org/ja/docs/DOM/BlobBuilder) (`MozBlobBuilder`) インタフェースが削除されました。今後 `Blob` オブジェクトを作成するには [`Blob`](https://developer.mozilla.org/ja/docs/DOM/Blob) コンストラクタを使用してください。
