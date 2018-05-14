---
title: "同期 `XMLHttpRequest` が廃止予定となりました"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
versions: ["30"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=969671"
      title: "Bug 969671 – Warn about use of sync XHR in the main thread"
---
[`XMLHttpRequest`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest) コンストラクターの `async` 引数は初期設定で `true` となっており、`false` に設定するとリクエストを同期に変更できます。メインスレッド上での [同期リクエスト](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/Synchronous_and_Asynchronous_Requests#Synchronous_request) の使用、つまり [Worker](https://developer.mozilla.org/docs/Web/Guide/Performance/Using_web_workers) 以外での使用は、ユーザー体験に悪影響を及ぼすことから廃止予定とされ、開発者向けの [ウェブコンソール](https://developer.mozilla.org/docs/Tools/Web_Console) に警告が出力されるようになりました。
