---
title: "Variables defined with `const` and `let` are no longer properties on `window`; redeclaration with `let` will throw"
date: "2015-10-13T20:37:00-04:00"
categories: ["javascript"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=589199": "Bug 589199 - Add an extra scope chain object for top-level script execution, encountered just before the global object, containing top-level |let| declaration bindings"
aliases:
    - "/docs/2015/variables-defined-with-const-and-let-are-no-longer-properties-on-window/"
---
As part of the ECMAScript 2015 (ES6) compliance, the behavior of the [`const`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const) and [`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) statements has been changed to match the spec.

Previously, global variables defined with those statements could be accessed as properties on the global object ([`window`](https://developer.mozilla.org/en-US/docs/Web/API/Window) or [`this`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this) in the global scope) like global variables defined with [`var`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var). This no longer works, so both `let x = 1; alert(window.x);` and `const y = 1; alert(window.y);` will be `undefined`, while `var z = 1; alert(window.z);` still dumps `1`. The easiest workwround here is to use `var` instead of `const` and `let`.

At the same time, redeclaration of global variables with `let` is now disallowed, therefore the following code snippets will no longer work:

```js
<script type="application/javascript;version=1.8">
  let a = 1;
  let a = 2; // raises TypeError
</script>
```

```js
<script type="application/javascript;version=1.8">
  let a = 1;
</script>
<script type="application/javascript;version=1.8">
  let a = 2; // raises TypeError
</script>
```

```js
<script type="application/javascript;version=1.8" src="let.js"></script>
<script type="application/javascript;version=1.8">
  let a = 2; // raises TypeError if a is defined in let.js
</script>
```

Also, code evaluated with the [`eval`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/eval) method will no longer propagate global variables defined with `let` or `const` to the outer context, therefore this also doesn't work:

```js
<script type="application/javascript;version=1.8">
  eval('let a = 1;');
  alert(a); // raises ReferenceError
</script>
```
