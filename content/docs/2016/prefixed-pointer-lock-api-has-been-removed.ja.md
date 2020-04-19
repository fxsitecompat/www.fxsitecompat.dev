---
title: "接頭辞付き Pointer Lock API が削除されました"
date: "2016-07-31T17:13:00-04:00"
categories: ["dom"]
tags: []
releases: ["50", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=991899"
      title: "Bug 991899 - Unprefix pointer lock"
---
[Pointer Lock API](https://developer.mozilla.org/docs/Web/API/Pointer_Lock_API) の仕様が安定したと思われることから、この API から接頭辞が外されました。これには、[pointerLockElement](https://developer.mozilla.org/docs/Web/API/Document/pointerLockElement) プロパティ、[requestPointerLock](https://developer.mozilla.org/docs/Web/API/Element/requestPointerLock)、[exitPointerLock](https://developer.mozilla.org/docs/Web/API/Document/exitPointerLock) 両メソッド、[pointerlockchange](https://developer.mozilla.org/docs/Web/Events/pointerlockchange)、[pointerlockerror](https://developer.mozilla.org/docs/Web/Events/pointerlockerror) 両イベントが含まれます。

同時に、`moz` 接頭辞付き API は移行期間なしに初期設定で無効化されました。Google Chrome は既に `webkit` 接頭辞付き API 対応を廃止していることから、互換性問題が起きることはないだろうと Mozilla 開発者は見ています。
