---
title: "Non-standard `String` generics have been deprecated"
date: "2016-12-10T17:45:00-05:00"
categories: ["javascript"]
tags: []
versions: ["53"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1319926"
      title: "Bug 1319926 - Warn when String generics are used"
aliases:
    - "/en-CA/docs/2016/non-standard-array-string-generics-have-been-deprecated/"
---
The non-standard, Firefox-specific [`String` generic methods](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String#String_generic_methods), introduced with [JavaScript 1.6](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.6), are now considered deprecated and will be removed in the near future. These generic/static methods include:

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
String.replace(num, search, replace);
// Alternative 1: the String global object
String(num).replace(search, replace);
// Alternative 2: the old-school way
String.prototype.replace.call(num, search, replace);
```

Note that the standard instance methods on [`String.prototype`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/prototype) won't be affected, of course. The following static methods are also in the ECMAScript 2015 (ES6) spec and therefore they won't be removed:

* [`String.fromCharCode`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode)
* [`String.fromCodePoint`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/fromCodePoint)
* [`String.raw`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/raw)

**Update**: `String` generics have been [removed with Firefox 68](https://www.fxsitecompat.com/en-CA/docs/2019/non-standard-string-generics-have-been-removed/).

**Update 2** The earlier version of this note mentioned `Array` generics as well, but `Array` generics have been officially deprecated since [Firefox 68](https://www.fxsitecompat.com/en-CA/docs/2016/non-array-string-generics-have-been-deprecated/), not Firefox 53. We have corrected the note.
