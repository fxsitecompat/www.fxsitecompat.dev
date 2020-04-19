---
title: "Legacy generator function is no longer allowed in method definitions"
date: "2016-08-08T08:58:00-04:00"
categories: ["javascript"]
tags: []
versions: ["51", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1199296"
      title: "Bug 1199296 - Don't allow legacy generator yield in method definitions"
---
Previously, it was possible to use the [`yield`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/yield) keyword in a [method definition](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/Method_definitions)'s getter to make it implicitly a [legacy generator function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/Legacy_generator_function). This is not valid according to the current ECMAScript spec, and therefore Firefox now raises a `SyntaxError`. Use [generator methods](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/Method_definitions#Shorthand_generator_methods) instead, as explained in [this newsgroup post](https://groups.google.com/d/topic/firefox-dev/2AklfAAFQuw/discussion).
