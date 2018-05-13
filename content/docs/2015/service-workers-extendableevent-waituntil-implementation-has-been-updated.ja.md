---
title: "Service Workers の `ExtendableEvent.waitUntil` 実装が更新されました"
date: "2015-09-25T00:21:00-04:00"
categories: ["dom"]
tags: []
versions: ["43"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1189644"
      title: "Bug 1189644 - \"Harness status: Timeout\" when running \"extendable-event-waituntil.https.html\" test"
---
[`ExtendableEvent.waitUntil`](https://developer.mozilla.org/docs/Web/API/ExtendableEvent/waitUntil) メソッドは、仕様に従い、その `ExtendableEvent` ハンドラーの外部で呼ばれた場合に `InvalidStateError` を投げます。また、`waitUntil` メソッドは複数の呼び出しを受け入れるようになり、その結果として得られる複数の [`Promise`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise) は [`Promise.all`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise/all) のように配列内で連鎖されます。
