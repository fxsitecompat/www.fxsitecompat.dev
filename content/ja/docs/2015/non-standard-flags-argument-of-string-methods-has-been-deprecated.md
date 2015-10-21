---
title: "`String` メソッドの非標準 `flags` 引数が廃止予定となりました"
date: "2015-03-17T14:02:59-04:00"
categories: ["javascript"]
tags: []
versions: ["39"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1142351": "Bug 1142351 - Add console warnings for non-standard flag argument of String.prototype.{search,match,replace}."
---
[`String.prototype.search`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/search)、[`match`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/match)、[`replace`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/replace) メソッドの非標準 `flags` 引数が廃止予定となり、近い将来削除されることとなりました。コード内でこの引数が使われていた場合、今後 [Web コンソール](https://developer.mozilla.org/ja/docs/Tools/Web_Console) に警告が出力されます。
