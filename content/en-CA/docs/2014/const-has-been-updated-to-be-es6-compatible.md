---
title: "`const` has been updated to be ES6 compatible"
date: "2014-12-19T11:15:21-05:00"
categories: ["javascript"]
tags: []
versions: ["36"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=611388"
      title: "Bug 611388 – const should be block-scoped and an initializer should be required"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1095439"
      title: "Bug 1095439 – Assigning to a const variable is a syntax error"
---
The support for [`const`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const) statement has been updated to comply with the ECMAScript 6 spec. First, it is now block-scoped like the [`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) statement, so `{ const a = 1 }; a;` will throw a [`ReferenceError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/ReferenceError) instead of just returning `1`. Second, it will require an initializer, so `const a;` now throws a [`SyntaxError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError). Third, it cannot be redeclared anymore, so `const a = 1; a = 2;` also throws a `SyntaxError`.
