---
title: "Array/generator comprehension support has been removed"
date: "2017-11-10T10:03:00-05:00"
categories: ["javascript"]
tags: []
versions: ["58", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1414340"
      title: "Bug 1414340 - Remove ES draft array/generator comprehensions"
---
The support for [array comprehensions](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Array_comprehensions) and [generator comprehensions](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Generator_comprehensions) has been removed with Firefox 58. Those were originally introduced with JavaScript 1.7 and 1.8, and later proposed as part of the ECMAScript 2015 draft that [replaced the legacy, non-standard syntaxes](https://www.fxsitecompat.dev/en-CA/docs/2016/legacy-array-generator-comprehension-syntaxes-have-been-removed/), but the newer syntaxes also failed to be standardized. Because both were not implemented by any other browsers, the compatibility risk should be very low.

Array comprehensions can be replaced with the [`Array.prototype.map`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map) and [`filter`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) methods. Generator comprehensions can also be replaced with [generator functions](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function*).
