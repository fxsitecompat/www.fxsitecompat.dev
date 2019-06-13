---
title: "非標準の `String` 汎用メソッドが廃止予定となりました"
date: "2016-12-10T17:45:00-05:00"
categories: ["javascript"]
tags: []
versions: ["53"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1319926"
      title: "Bug 1319926 - Warn when String generics are used"
aliases:
    - "/ja/docs/2016/non-standard-array-string-generics-have-been-deprecated/"
---
[JavaScript 1.6](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.6) で導入された非標準で Firefox 独自の [`String` 汎用メソッド](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String#String_generic_methods) は廃止予定となり、近い将来削除されることとなりました。これらの汎用・静的メソッドには以下のものが含まれます。

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

以下に汎用メソッドの代替策をいくつか挙げます。

```js
// 非推奨
String.replace(num, search, replace);
// 代替策 1: String グローバルオブジェクト
String(num).replace(search, replace);
// 代替策 2: 昔ながらの方法
String.prototype.replace.call(num, search, replace);
```

なお、[`String.prototype`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/prototype) 上の標準インスタンスメソッドには当然ながら影響はありません。以下の静的メソッドも ECMAScript 2015 (ES6) 仕様に含まれており、削除される予定はありません。

* [`String.fromCharCode`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode)
* [`String.fromCodePoint`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/fromCodePoint)
* [`String.raw`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/raw)

**更新**: `String` 汎用メソッドは [Firefox 68 で削除されました](https://www.fxsitecompat.dev/ja/docs/2019/non-standard-string-generics-have-been-removed/)。

**更新 2** この記事の初期バージョンは `Array` 汎用メソッドにも言及していましたが、`Array` 汎用メソッドは Firefox 53 ではなく [Firefox 68](https://www.fxsitecompat.dev/ja/docs/2016/non-array-string-generics-have-been-deprecated/) 以降公式に廃止予定となりました。この記事は訂正済みです。
