---
title: "非標準の `Array` 汎用メソッドが削除されました"
date: "2019-09-30T16:46:00-04:00"
categories: ["javascript"]
tags: []
releases: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1222547"
      title: "Bug 1222547 - Remove Array generics"
---
[JavaScript 1.6](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.6) で導入され、[Firefox 68](https://www.fxsitecompat.dev/ja/docs/2019/non-standard-array-generics-have-been-deprecated/) 以降廃止予定となっていた非標準で Firefox 独自の [`Array` 汎用メソッド](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array#Array_generic_methods) は、Firefox 71 で削除されました。これらの汎用・静的メソッドには以下のものが含まれます。

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

以下に汎用メソッドの代替策をいくつか挙げます。

```js
// 非推奨
Array.forEach(obj, callback);
// 代替策 1: スプレッド構文
[...obj].forEach(callback);
// 代替策 2: Array.from メソッド
Array.from(obj).forEach(callback);
// 代替策 3: 昔ながらの方法
// (オブジェクトがまだ反復可能となっていない場合)
Array.prototype.forEach.call(obj, callback);
```

なお、[`Array.prototype`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/prototype) 上の標準インスタンスメソッドには当然ながら影響はありません。以下の静的メソッドも ECMAScript 2015 (ES6) 仕様に含まれており、削除される予定はありません。

* [`Array.from`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/from)
* [`Array.isArray`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/isArray)
* [`Array.of`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/of)
