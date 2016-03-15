---
title: "Legacy iterator and generator support will be removed"
date: "2015-10-26T13:56:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=881061"
      title: "Bug 881061 - Remove Iterator"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083482"
      title: "Bug 1083482 - Remove SpiderMonkey support for JS1.7 legacy generators"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1104014"
      title: "Bug 1104014 - Disable old-style generators in web content"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1119777"
      title: "Bug 1119777 - Remove non-standard Function.prototype.isGenerator"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1199296"
      title: "Bug 1199296 - Don't allow legacy generator yield in method definitions"
aliases:
    - "/docs/2015/iterator-method-will-be-removed/"
---
The support for the non-standard iterators and generators, introduced with [JavaScript 1.7](https://developer.mozilla.org/en-US/docs/Web/JavaScript/New_in_JavaScript/1.7), will be removed in the future. Those include the [`Iterator`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Iterator) object, `__iterator__` method, [`StopIteration`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/StopIteration) object, [`Function.prototype.isGenerator`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/isGenerator) method, [legacy generator function statement](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/Legacy_generator_function), [legacy generator function expression](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Legacy_generator_function), [legacy generator objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator#Legacy_generator_objects) and [generator comprehensions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Generator_comprehensions). Learn about the [standard iterators and generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators) for the alternatives.

ECMAScript 2015 (ES6) offers several iterable objects, including [`Array`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array), [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) and [`Set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set), and various DOM APIs, including [`StyleSheetList`](https://developer.mozilla.org/en-US/docs/Web/API/Document/styleSheets) (since [Firefox 31](https://bugzilla.mozilla.org/show_bug.cgi?id=738196)), [`CSSRuleList`](https://developer.mozilla.org/en-US/docs/Web/API/CSSRuleList) (since [Firefox 32](https://bugzilla.mozilla.org/show_bug.cgi?id=995664)), [`URLSearchParams`](https://developer.mozilla.org/en-US/docs/Web/API/URLSearchParams) (since [Firefox 44](https://bugzilla.mozilla.org/show_bug.cgi?id=1085284)) and [`FormData`](https://developer.mozilla.org/en-US/docs/Web/API/FormData) (since [Firefox 44](https://bugzilla.mozilla.org/show_bug.cgi?id=1127703)), are now iterable. Those can be used in conjunction with the [`for...of`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of) statement without `Iterator`. For generic, non-iterable objects, you can simply replace the non-standard `Iterator` object with the new, standard [`Object.entries`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/entries) method to make them iterable.
