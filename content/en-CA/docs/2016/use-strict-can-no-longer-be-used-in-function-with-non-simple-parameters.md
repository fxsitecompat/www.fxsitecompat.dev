---
title: "`use strict` can no longer be used in function with non-simple parameters"
date: "2016-10-25T10:28:00-04:00"
categories: ["javascript"]
tags: []
versions: ["52"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1272784"
      title: "Bug 1272784 - |function f(a = 1) { \"use strict\"; }| should throw Early Error."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/jAWMy-W_AaY/discussion"
      title: "Intent to unship: Use strict in function with non-simple parameters"
---
According to the ECMAScript 2016 spec, the `"use strict";` statement that invokes [strict mode](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode) cannot be used in a function with [default parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters) or [rest parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters). Firefox 52 and later will throw a `SyntaxError` for such cases. Since Google Chrome and Microsoft Edge have already made the change, the compatibility impact should be minimum.
