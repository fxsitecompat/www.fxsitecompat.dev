---
title: "Non-standard `Array` generics have been removed"
date: "2019-09-30T16:46:00-04:00"
categories: ["javascript"]
tags: []
versions: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1222547"
      title: "Bug 1222547 - Remove Array generics"
---
The non-standard, Firefox-specific [`Array` generic methods](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array#Array_generic_methods), introduced with [JavaScript 1.6](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.6) and deprecated since [Firefox 68](https://www.fxsitecompat.dev/en-CA/docs/2019/non-standard-array-generics-have-been-deprecated/), have been removed with Firefox 71. These generic/static methods include:

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

Note that the standard instance methods on [`Array.prototype`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/prototype) won't be affected, of course. The following static methods are also in the ECMAScript 2015 (ES6) spec and therefore they won't be removed:

* [`Array.from`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/from)
* [`Array.isArray`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/isArray)
* [`Array.of`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/of)
