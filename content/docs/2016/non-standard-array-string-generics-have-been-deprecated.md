---
title: "Non-standard `Array`/`String` generics have been deprecated"
date: "2016-12-10T17:45:00-05:00"
categories: ["javascript"]
tags: []
versions: ["53"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1319926"
      title: "Bug 1319926 - Warn when String generics are used"
---
The non-standard, Firefox-specific [`Array` generic methods](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array#Array_generic_methods) and [`String` generic methods](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String#String_generic_methods), introduced with [JavaScript 1.6](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.6), are now considered deprecated and will be [removed in the near future](https://www.fxsitecompat.com/en-CA/docs/2015/non-standard-array-string-generics-will-be-removed/). These generic/static methods include:

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

Here are some alternatives to the generics:

```js
// Deprecated
Array.forEach(obj, callback);
// Alternative 1: the spread syntax
[...obj].forEach(callback);
// Alternative 2: the Array.from method
Array.from(obj).forEach(callback);
// Alternative 3: the old-school way
// (if the object is not yet iterable)
Array.prototype.forEach.call(obj, callback);
```

```js
// Deprecated
String.replace(num, search, replace);
// Alternative 1: the String global object
String(num).replace(search, replace);
// Alternative 2: the old-school way
String.prototype.replace.call(num, search, replace);
```

Note that the standard instance methods on [`Array.prototype`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/prototype) and [`String.prototype`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/prototype) won't be affected, of course. The following static methods are also in the ECMAScript 2015 (ES6) spec and therefore they won't be removed:

* [`Array.from`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/from)
* [`Array.isArray`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/isArray)
* [`Array.of`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/of)
* [`String.fromCharCode`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode)
* [`String.fromCodePoint`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/fromCodePoint)
* [`String.raw`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/raw)
