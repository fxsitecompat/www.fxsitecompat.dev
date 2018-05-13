---
title: "ブロックスコープ内関数の再宣言が廃止予定となりました"
date: "2016-01-24T17:52:00-05:00"
categories: ["javascript"]
tags: []
versions: ["46"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1071646"
      title: "Bug 1071646 - Implement ES6 block-level functions"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1235590"
      title: "Bug 1235590 - idbroker.webex.com sign up form and log-in broken"
---
Firefox 46 で、[`let`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/let) 宣言と同様の挙動となる ES6 互換のブロックレベル関数が実装されました。これにより、同一スコープ内に同名の関数が複数存在した場合は `SyntaxError` が投げられます。しかし、サイト互換性問題によりこの制約は一時的に緩和され、代わりに廃止警告がコンソールへ出力されるだけとなりました。この過渡的措置は近い将来削除されます。
