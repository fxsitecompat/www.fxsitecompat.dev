---
title: "ECMAScript `arguments` implementation has been updated"
date: "2015-09-24T17:00:00-04:00"
categories: ["javascript"]
tags: []
versions: ["43"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=889158"
      title: "Bug 889158 - Calling an arrow function shouldn't create an 'arguments' binding"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1175394"
      title: "Bug 1175394 - Mapped arguments object should only be created when its FormalParameters is a SimpleParameterList"
---
As part of the ECMAScript 2015 (ES6) compliance, [arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions) no longer have their own [`arguments`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments). The `arguments` object will rather be inherited from the outer function if any. The [rest parameter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters) syntax can be used to access the actual arguments of arrow functions.

Also, starting with Firefox 43, a *mapped* `arguments` object will be provided only when the code is in the non-[strict mode](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode) and the function doesn't have any rest parameters, [default parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters) or [destructured parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#Function_argument_defaults). See an [example](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments#Rest_default_and_destructured_parameters) on the MDC document.
