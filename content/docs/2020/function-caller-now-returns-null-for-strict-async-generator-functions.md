---
title: "`Function.caller` now returns `null` for strict, async, generator functions"
date: "2020-02-13T22:52:00-05:00"
categories: ["javascript"]
tags: []
releases: ["75"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1610206"
      title: "Bug 1610206 - Restrict functions returned by Function#caller"
---
Firefox 75 has changed the behaviour of the [`Function.caller`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/caller) property to align with the latest ECMAScript spec proposal. It was previously throwing a `TypeError` when the caller was a [strict function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Strict_mode). Starting with Firefox 75, the property will return `null` for such cases. The same applies to [async functions](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/async_function) and [generator functions](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function*) where access to the caller was not restricted before.

```js
function x() {
  console.log(x.caller);
}
// All the following functions now logging `null`
(function s() {
  "use strict";
  x(); // Previously throwing
})();
(async function a() {
  x(); // Previously logging `a()`
})();
(function* g() {
  yield x(); // Previously logging `g()`
}().next());
```
