---
title: "`Array`/`String` 汎用メソッドが削除されます"
date: "2015-11-06T16:08:00-08:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1222547"
      title: "Bug 1222547 - Remove Array generics"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1222552"
      title: "Bug 1222552 - Remove String generics"
---
[JavaScript 1.6](https://developer.mozilla.org/ja/docs/Web/JavaScript/New_in_JavaScript/1.6) で導入された非標準の [`Array` 汎用メソッド](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array#Array_generic_methods) と [`String` 汎用メソッド](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String#String_generic_methods) は、将来的に削除されます。

`Array` 汎用メソッドの単純な代替としては [スプレッド演算子](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Spread_operator) があります。例えば、`Array.every(str, callback)` は `[...str].every(callback)` のように書き換えられます。

`String` 汎用メソッドの単純な代替としては [`String`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String) グローバルオブジェクトがあります。例えば、`String.replace(num, search, replace)` は `String(num).replace(search, replace)` のように書き換えられます。
