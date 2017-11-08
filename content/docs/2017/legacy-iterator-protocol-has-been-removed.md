---
title: "Legacy iterator protocol has been removed"
date: "2017-09-20T18:52:00-04:00"
categories: ["javascript"]
tags: []
versions: ["57"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1098412"
      title: "Bug 1098412 - Remove __iterator__ and the legacy Iterator constructor"
---
The support for the non-standard, legacy iterator protocol, introduced with [JavaScript 1.7](https://developer.mozilla.org/en-US/docs/Web/JavaScript/New_in_JavaScript/1.7), has been removed with Firefox 57. This includes the [`Iterator`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Iterator) constructor and `__iterator__` method.

ECMAScript 2015 (ES6) offers the iterable [`Array`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array), [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) and [`Set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set) objects, and various DOM APIs are now also iterable, such as [`StyleSheetList`](https://developer.mozilla.org/en-US/docs/Web/API/StyleSheetList) (since [Firefox 31](https://bugzilla.mozilla.org/show_bug.cgi?id=738196)), [`CSSRuleList`](https://developer.mozilla.org/en-US/docs/Web/API/CSSRuleList) (since [Firefox 32](https://bugzilla.mozilla.org/show_bug.cgi?id=995664)), [`URLSearchParams`](https://developer.mozilla.org/en-US/docs/Web/API/URLSearchParams) (since [Firefox 44](https://bugzilla.mozilla.org/show_bug.cgi?id=1085284)), [`FormData`](https://developer.mozilla.org/en-US/docs/Web/API/FormData) (since [Firefox 44](https://bugzilla.mozilla.org/show_bug.cgi?id=1127703)), [`Headers`](https://developer.mozilla.org/en-US/docs/Web/API/Headers) (since [Firefox 44](https://bugzilla.mozilla.org/show_bug.cgi?id=1108181)), [`NodeList`](https://developer.mozilla.org/en-US/docs/Web/API/NodeList) and [`DOMTokenList`](https://developer.mozilla.org/en-US/docs/Web/API/DOMTokenList) (since [Firefox 50](https://bugzilla.mozilla.org/show_bug.cgi?id=1290636)).

Those objects can be used in conjunction with the [`for...of`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of) statement without the `Iterator` constructor. For generic, non-iterable objects, you can simply replace `Iterator` with the new, standard [`Object.entries`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/entries) method to make them iterable. See the [standard iterators and generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators) for details.
