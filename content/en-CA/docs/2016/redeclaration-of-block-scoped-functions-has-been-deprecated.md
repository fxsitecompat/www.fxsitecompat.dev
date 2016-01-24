---
title: "Redeclaration of block-scoped functions has been deprecated"
date: "2016-01-24T17:52:00-05:00"
categories: ["javascript"]
tags: []
versions: ["46"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1071646": "Bug 1071646 - Implement ES6 block-level functions"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1235590": "Bug 1235590 - idbroker.webex.com sign up form and log-in broken"
---
Firefox 46 has implemented ES6-compatible block-level functions that behave in the same way as [`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) declarations. It means having the same name functions in the same scope will raise a `SyntaxError`. However, the constraint has been temporarily relaxed due to site compatibility issues, just logging a deprecation warning instead. This transitional measure will be removed with Firefox 50.
