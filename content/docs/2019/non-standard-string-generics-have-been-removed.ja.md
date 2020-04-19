---
title: "非標準の `String` 汎用メソッドが廃止されました"
date: "2019-05-28T05:38:00-04:00"
categories: ["javascript"]
tags: []
versions: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1222552"
      title: "Bug 1222552 - Remove String generics"
aliases:
    - "/ja/docs/2015/array-string-generics-will-be-removed/"
    - "/ja/docs/2015/non-standard-array-string-generics-will-be-removed/"
---
[JavaScript 1.6](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.6) で導入され、[Firefox 53](https://www.fxsitecompat.dev/ja/docs/2016/non-standard-string-generics-have-been-deprecated/) 以降廃止予定となっていた非標準の `String` 汎用メソッドが Firefox 68 で削除されました。これには以下のものが含まれます。

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

`String` 汎用メソッドの単純な代替としては `String` グローバルオブジェクトがあります。例えば、`String.replace(num, search, replace)` は `String(num).replace(search, replace)` のように書き換えられます。

以下の標準静的メソッドは引き続き使用可能です。

* `String.fromCharCode`
* `String.fromCodePoint`
* `String.raw`

非標準 `Array` 汎用メソッドも [近い将来削除されます](https://www.fxsitecompat.dev/ja/docs/2019/non-standard-array-generics-have-been-deprecated/)。
