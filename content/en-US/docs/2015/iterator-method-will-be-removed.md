---
title: "`Iterator` method will be removed"
date: "2015-10-26T13:56:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=881061": "Bug 881061 - Remove Iterator"
---
The non-standard [`Iterator`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Iterator) method, introduced with [JavaScript 1.7](https://developer.mozilla.org/en-US/docs/Web/JavaScript/New_in_JavaScript/1.7) and used to make any objects [iterable](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators), will be removed in the future. It has never been standardized nor implemented in other browsers.

ECMAScript 2015 (ES6) offers several iterable objects, including [`Array`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array), [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) and [`Set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set), and various DOM APIs, including [`StyleSheetList`](https://developer.mozilla.org/en-US/docs/Web/API/Document/styleSheets) (since [Firefox 31](https://bugzilla.mozilla.org/show_bug.cgi?id=738196)), [`CSSRuleList`](https://developer.mozilla.org/en-US/docs/Web/API/CSSRuleList) (since [Firefox 32](https://bugzilla.mozilla.org/show_bug.cgi?id=995664)), [`URLSearchParams`](https://developer.mozilla.org/en-US/docs/Web/API/URLSearchParams) (since [Firefox 44](https://bugzilla.mozilla.org/show_bug.cgi?id=1085284)) and [`FormData`](https://developer.mozilla.org/en-US/docs/Web/API/FormData) (since [Firefox 44](https://bugzilla.mozilla.org/show_bug.cgi?id=1127703)), are now iterable. Those can be used in conjunction with the [`for...of`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of) statement without `Iterator`.

The generic [`Object`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) is not iterable unlike other objects, so you have to use the traditional [`for...in`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in) statement to iterate over the properties.
