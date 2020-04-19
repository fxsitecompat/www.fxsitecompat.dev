---
title: "配列分割代入で残余要素の末尾にコンマが続いた場合、例外が投げられます"
date: "2016-10-23T17:55:00-04:00"
categories: ["javascript"]
tags: []
releases: ["52", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1041341"
      title: "Bug 1041341 - Make `[...rest,] = []` a SyntaxError"
---
[配列分割代入構文](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#Array_destructuring) の左辺に何らかの [残余要素](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Spread_operator#Rest_operator) が含まれ、その末尾にコンマが続いた場合、Firefox 52 以降では ECMAScript 2015 (ES6) 仕様に従って `SyntaxError` が投げられます。

```js
let [a, b, c, ...rest,] = [1, 2, 3, 4, 5]; // SyntaxError
```
