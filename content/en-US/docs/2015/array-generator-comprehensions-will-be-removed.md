---
title: "Array/generator comprehensions will be removed"
date: "2015-11-02T01:48:00-08:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1220564": "Bug 1220564 - Remove non-standard array/generator comprehension."
---
The support for [array comprehensions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Array_comprehensions) and [generator comprehensions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Generator_comprehensions) will be removed in the future. These syntaxes have been proposed by Mozilla but failed to be standardized in ECMAScript. The [`Array.prototype.map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map), [`filter`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) methods and [arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions) can be used instead of array comprehensions. The [`function*`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*) declaration can be used instead of generator comprehensions.
