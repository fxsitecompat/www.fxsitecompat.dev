---
title: "`Proxy` ハンドラーが特定の状況で例外を投げるようになりました"
date: "2015-03-17T14:02:59-04:00"
categories: ["javascript"]
tags: []
releases: ["39", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1132522"
      title: "Bug 1132522 - Treat false return value from certain Proxy handler methods as failure"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=828137"
      title: "Bug 828137 - Need APIs that would allow proxies to implement Reject in spec terms"
---
[`Proxy`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy) オブジェクトの実装が ES6 仕様により忠実に準拠するよう更新されました。今後 [Strict モード](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Strict_mode) で [`defineProperty`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy/handler/defineProperty)、[`set`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy/handler/set) 両ハンドラーを成功させるには明示的に `true` を返す必要があり、それ以外の場合は [`TypeError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/TypeError) 例外が投げられます。また、[`window`](https://developer.mozilla.org/docs/Web/API/Window) オブジェクトがこれらのハンドラーのターゲットに設定されていた場合も、Firefox 39 以降 `TypeError` が投げられます。
