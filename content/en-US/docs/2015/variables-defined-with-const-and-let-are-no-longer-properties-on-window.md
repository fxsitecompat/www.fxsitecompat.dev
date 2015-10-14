---
title: "Variables defined with `const` and `let` are no longer properties on `window`"
date: "2015-10-13T20:37:00-04:00"
categories: ["javascript"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=589199": "Bug 589199 - Add an extra scope chain object for top-level script execution, encountered just before the global object, containing top-level |let| declaration bindings"
---
As part of the ECMAScript 2015 (ES6) compliance, the behavior of the [`const`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const) and [`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) statements has been changed to match the spec.

Previously, variables defined with those statements could be accessed as properties on the global object ([`window`](https://developer.mozilla.org/en-US/docs/Web/API/Window) or [`this`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this) in the global scope) like variables defined with [`var`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var). This no longer works, so both `let x = 1; alert(window.x);` and `const y = 1; alert(window.y);` will be `undefined`, while `var z = 1; alert(window.z);` still dumps `1`. The easiest workwround here is to use `var` instead of `const` and `let`.
