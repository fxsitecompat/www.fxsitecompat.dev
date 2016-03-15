---
title: "`RegExp.multiline` グローバルスイッチが削除されます"
date: "2015-12-19T01:10:00-05:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1219757"
      title: "Bug 1219757 - Remove nonstandard RegExp.multiline global switch"
---
[Firefox 46 以降廃止予定となっている](https://www.fxsitecompat.com/ja/docs/2015/regexp-multiline-global-switch-has-been-deprecated/) [`RegExp`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/RegExp) オブジェクト上の非標準 `multiline` プロパティが、近い将来削除されます。`RegExp` リテラルとコンストラクタの `m` フラグを代わりに使用してください。なお、`RegExp` インスタンス上の標準 [`multiline`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/RegExp/multiline) プロパティは削除されません。
