---
title: "Setting properties on a primitive now throws in strict mode"
date: "2016-03-28T12:25:00-04:00"
categories: ["javascript"]
tags: []
versions: ["46"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=603201"
      title: "Bug 603201 - Strict getters on primitive wrapper prototypes receive wrapped |this| values"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1240792"
      title: "Bug 1240792 - Add a test for assigning to primitives in strict mode"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1241966"
      title: "Bug 1241966 - Better error when assigning to primitives in strict mode"
    - url: "https://groups.google.com/d/topic/mozilla.dev.tech.js-engine/O3qHW_hJ3Sk/discussion"
      title: "\"use strict\" behaviour change in 46 - mozilla.dev.tech.js-engine"
---
Previously, setting properties on a [primitive value](https://developer.mozilla.org/en-US/docs/Glossary/Primitive), including [`String`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String), [`Number`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number), [`Boolean`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) and [`Symbol`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol), resulted in a no-op (did nothing). On Firefox 46 and later, such code in [strict mode](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode) will throw a [`TypeError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError) according to the ECMAScript 2015 (ES6) spec. See the examples below:

```js
(function() {
  "use strict";
  10.sub = 5; // TypeError
})();
```
```js
(function() {
  "use strict";
  false.x = false; // TypeError
})();
```
```js
(function() {
  "use strict";
  "test".mode = "verbose"; // TypeError
})();
```
```js
(function() {
  "use strict";
  Symbol().check = true; // TypeError
})();
```
