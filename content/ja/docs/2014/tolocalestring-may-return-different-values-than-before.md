---
title: "`toLocaleString` が従来と異なる値を返す可能性があります"
date: "2014-02-07T11:57:09-05:00"
categories: ["javascript"]
tags: []
versions: ["29"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=837963": "Bug 837963 – [meta] Implement ECMAScript Internationalization API"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=769871": "Bug 769871 – Reimplement String.localeCompare, Number.toLocaleString, Date.toLocaleString per ECMA-402"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=999003": "Bug 999003 – toLocaleString with undefined locale uses localized digits specified by the OS"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1010535": "Bug 1010535 – (new Date()).toLocaleString() changed format"
---
[`Date.toLocaleString`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleString)、[`Date.toLocaleDateString`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString)、[`Date.toLocaleTimeString`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleTimeString)、[`Number.toLocaleString`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Number/toLocaleString)、[`String.localeCompare`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/localeCompare) の各メソッドが、ECMAScript Internationalization API に対応するため再実装されました。これらのメソッドは引数が省略された場合実装依存となり、Firefox の旧バージョンが返していた値とは異なる結果になる可能性があります。

これまで、`Date.toLocaleString`、`Date.toLocaleDateString` and `Date.toLocaleTimeString` はシステムの日時を返していましたが、この変更により、ブラウザのロケールによって形式が変わるようになりました。`Number.toLocaleString` は、Firefox の旧バージョンでは英語の数字を返していましたが、今後は OS 定義のローカライズされた数字を返します。`String.localeCompare` は、従来 `2` や `-2` が返されていたところ、`1` や `-1` を返す可能性があります。
