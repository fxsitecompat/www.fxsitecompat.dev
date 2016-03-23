---
title: "`RegExp.multiline` グローバルスイッチが削除されました"
date: "2016-03-23T05:30:00-04:00"
categories: ["javascript"]
tags: []
versions: ["48"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1219757"
      title: "Bug 1219757 - Remove nonstandard RegExp.multiline global switch"
aliases:
    - "/docs/2015/regexp-multiline-global-switch-will-be-removed/"
---
[Firefox 46 以降廃止予定となっていた](https://www.fxsitecompat.com/ja/docs/2015/regexp-multiline-global-switch-has-been-deprecated/) [`RegExp`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/RegExp) オブジェクト上の非標準 `multiline` プロパティが、Firefox 48 で削除されました。`RegExp` リテラルとコンストラクタの `m` フラグを代わりに使用してください。なお、`RegExp` インスタンス上の標準 [`multiline`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/RegExp/multiline) プロパティは削除されません。
