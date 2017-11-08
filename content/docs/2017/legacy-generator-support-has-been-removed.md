---
title: "Legacy generator support has been removed"
date: "2017-11-08T15:15:00-05:00"
categories: ["javascript"]
tags: []
versions: ["58"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083476"
      title: "Bug 1083476 - Add console warnings for JS1.7 legacy generators"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083482"
      title: "Bug 1083482 - Remove SpiderMonkey support for JS1.7 legacy generators"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1119777"
      title: "Bug 1119777 - Remove non-standard Function.prototype.isGenerator"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1413867"
      title: "Bug 1413867 - Remove StopIteration"
aliases:
    - "/en-CA/docs/2015/iterator-method-will-be-removed/"
    - "/en-CA/docs/2015/legacy-iterator-and-generator-support-will-be-removed/"
---
The support for the non-standard generators, introduced with [JavaScript 1.7](https://developer.mozilla.org/en-US/docs/Web/JavaScript/New_in_JavaScript/1.7) and deprecated since Firefox 57, has been removed with Firefox 58. This includes the [`StopIteration`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/StopIteration) object, [`Function.prototype.isGenerator`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/isGenerator) method, [legacy generator function statement](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/Legacy_generator_function), [legacy generator function expression](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Legacy_generator_function), [legacy generator objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator#Legacy_generator_objects) and [generator comprehensions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Generator_comprehensions).

The legacy iterator protocol support has already been removed with [Firefox 57](https://www.fxsitecompat.com/en-CA/docs/2017/legacy-iterator-protocol-has-been-removed/). Learn about the [standard iterators and generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators) for the alternatives.
