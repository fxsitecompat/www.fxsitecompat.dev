---
title: "Array destructuring with rest element will throw if trailing comma follows"
date: "2016-10-23T17:55:00-04:00"
categories: ["javascript"]
tags: []
releases: ["52", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1041341"
      title: "Bug 1041341 - Make `[...rest,] = []` a SyntaxError"
---
Firefox 52 and later will throw a `SyntaxError` if the left-hand side of the [array destructuring assignment syntax](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#Array_destructuring) contains any [rest element](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Spread_operator#Rest_operator) followed by a trailing comma, according to the ECMAScript 2015 (ES6) spec.

```js
let [a, b, c, ...rest,] = [1, 2, 3, 4, 5]; // SyntaxError
```
