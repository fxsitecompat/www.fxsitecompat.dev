---
title: "正規表現のキャプチャ動作が変更されました"
date: "2014-09-01T22:12:15-04:00"
categories: ["javascript"]
tags: []
versions: ["34"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=369778": "Bug 369778 – Javascript regular expression captures broken with alternation in some cases."
---
`String.replace` を含む正規表現において、数量詞によってキャプチャグループの参照が妨げられた場合、そのグループの一致テキストが空文字列の代わりに `undefined` となります ([このサンプルコード](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/RegExp#Gecko-specific_notes) も参照してください)。なお、後方互換性のため、`RegExp.$N` は引き続き `undefined` ではなく空文字列を返します ([Bug 1053944](https://bugzilla.mozilla.org/show_bug.cgi?id=1053944))。

Firefox 32 で発生した正規表現のパフォーマンスリグレッションも Firefox 34 で修正されました。この問題は、例えば [`String.match`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/match) を使った場合に、Firefox 32、33 上で「応答のないスクリプト」ダイアログを表示させる可能性がありました。
