---
title: "`Proxy` が関数に変更されました"
date: "2013-07-14T19:12:37-04:00"
categories: ["javascript"]
tags: []
releases: ["25", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=788172"
      title: "Bug 788172 – Proxy is not a function (typeof Proxy should be \'function\')"
---
[`Proxy`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy) インターフェイスがオブジェクトから関数に変更され、[`new`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/new) 演算子抜きでも呼び出し可能となりました。機能判別のため [`typeof`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/typeof) 演算子を使っている場合、`typeof Proxy` が `"function"` を返すようになるため、注意が必要かもしれません。
