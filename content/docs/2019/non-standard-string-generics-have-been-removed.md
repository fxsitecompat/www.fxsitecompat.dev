---
title: "Non-standard `String` generics have been removed"
date: "2019-05-28T05:38:00-04:00"
categories: ["javascript"]
tags: []
versions: ["68"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1222552"
      title: "Bug 1222552 - Remove String generics"
aliases:
    - "/en-CA/docs/2015/array-string-generics-will-be-removed/"
    - "/en-CA/docs/2015/non-standard-array-string-generics-will-be-removed/"
---
The non-standard `String` generic methods, introduced with [JavaScript 1.6](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.6) and deprecated since [Firefox 53](https://www.fxsitecompat.com/en-CA/docs/2016/non-standard-array-string-generics-have-been-deprecated/), have been removed with Firefox 68. This includes:

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

The `String` global object can be used as a simple alternative to the `String` generics. For example, `String.replace(num, search, replace)` can be replaced with `String(num).replace(search, replace)`.

The following standard static methods will remain available:

* `String.fromCharCode`
* `String.fromCodePoint`
* `String.raw`

The non-standard `Array` generic methods will also be removed in the near future.
