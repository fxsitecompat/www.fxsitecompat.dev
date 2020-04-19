---
title: "Destructuring `for-in` loop has been removed"
date: "2015-04-27T13:17:23-04:00"
categories: ["javascript"]
tags: []
versions: ["40", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083498"
      title: "Bug 1083498 - Remove SpiderMonkey support for destructuring for-in (JS1.7-only language extension)"
---
The non-standard implementation of destructuring [`for...in`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...in) loops in JavaScript 1.7, like `for (var/let/const [key, value] in object)`, has been removed. For an [`Array`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array) or other [iterable objects](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Iteration_protocols), you can simply use the [`for...of`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of) loop instead. For a general [`Object`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object), you can also use the `for...of` loop in combination with [`Iterator`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Iterator), like `for (let [key, value] of Iterator(object))`, but unfortunately the non-standard `Iterator` will also be removed in the future. Therefore, a realistic solution might be `for (let key in obj) { let value = obj[key]; }`.
