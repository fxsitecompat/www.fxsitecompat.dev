---
title: "Strict モードでのプリミティブへのプロパティ設定が例外を投げるようになりました"
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
従来、[`String`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String)、[`Number`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Number)、[`Boolean`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Boolean)、[`Symbol`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Symbol) といった [プリミティブ値](https://developer.mozilla.org/ja/docs/Glossary/Primitive) へのプロパティ設定は無演算命令 (何もしない) となっていました。Firefox 46 以降、[Strict モード](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Strict_mode) 内でそうしたコードが見られた場合、ECMAScript 2015 (ES6) 仕様に従って [`TypeError`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/TypeError) が投げられます。以下の例を参照してください。

```js
(function() {
  "use strict";
  (10).sub = 5; // TypeError
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
