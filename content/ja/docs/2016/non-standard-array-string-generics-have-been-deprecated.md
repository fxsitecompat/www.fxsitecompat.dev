---
title: "非標準の `Array`/`String` 汎用メソッドが廃止予定となりました"
date: "2016-12-10T17:45:00-05:00"
categories: ["javascript"]
tags: []
versions: ["53"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1319926"
      title: "Bug 1319926 - Warn when String generics are used"
---
[JavaScript 1.6](https://developer.mozilla.org/ja/docs/Web/JavaScript/New_in_JavaScript/1.6) で導入された非標準の [`Array` 汎用メソッド](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array#Array_generic_methods) と [`String` 汎用メソッド](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String#String_generic_methods) は廃止予定となり、[近い将来削除されることとなりました](https://www.fxsitecompat.com/ja/docs/2015/non-standard-array-string-generics-will-be-removed/)。これには以下のものが含まれます。

* `Array.concat`
* `Array.every`
* `Array.filter`
* `Array.forEach`
* `Array.indexOf`
* `Array.join`
* `Array.lastIndexOf`
* `Array.map`
* `Array.pop`
* `Array.push`
* `Array.reduce`
* `Array.reduceRight`
* `Array.reverse`
* `Array.shift`
* `Array.slice`
* `Array.some`
* `Array.sort`
* `Array.splice`
* `Array.unshift`
* `String.charAt`
* `String.charCodeAt`
* `String.concat`
* `String.endsWith`
* `String.includes`
* `String.indexOf`
* `String.lastIndexOf`
* `String.localeCompare`
* `String.match`
* `String.normalize`
* `String.replace`
* `String.search`
* `String.slice`
* `String.split`
* `String.startsWith`
* `String.substr`
* `String.substring`
* `String.toLocaleLowerCase`
* `String.toLocaleUpperCase`
* `String.toLowerCase`
* `String.toUpperCase`
* `String.trim`
* `String.trimLeft`
* `String.trimRight`

`Array` 汎用メソッドの単純な代替としては [スプレッド演算子](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Spread_operator) があります。例えば、`Array.every(str, callback)` は `[...str].every(callback)` のように書き換えられます。

`String` 汎用メソッドの単純な代替としては [`String`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String) グローバルオブジェクトがあります。例えば、`String.replace(num, search, replace)` は `String(num).replace(search, replace)` のように書き換えられます。

なお、以下の汎用メソッドは ECMAScript 2015 (ES6) 仕様に含まれており、削除される予定はありません。

* [`Array.from`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/from)
* [`Array.isArray`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/isArray)
* [`Array.of`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/of)
* [`String.fromCharCode`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode)
* [`String.fromCodePoint`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/fromCodePoint)
* [`String.raw`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/raw)
