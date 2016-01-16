---
title: "ES6-compatible `let` disallows variable redeclaration"
date: "2014-10-17T22:50:44-04:00"
categories: ["javascript"]
tags: []
versions: ["35"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1001090": "Bug 1001090 – Implement ES6 \"temporal dead zone\" for let"
---
The [`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) statement implementation has been updated to support the "[temporal dead zone](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let#Temporal_dead_zone_and_errors_with_let)" of the ECMAScript 6 spec, though the implementation is not yet fully ES6-compatible. Starting with Firefox 35, redeclaring an existing variable in the same block scope throws a [`TypeError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError), while referring a variable before the variable is declared raises a [`ReferenceError`](https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Global_Objects/ReferenceError). This change will mainly affect [Open Web Apps](https://developer.mozilla.org/en-US/Apps) for Firefox and Firefox OS, as well as [Firefox extensions](https://developer.mozilla.org/en-US/Add-ons). See also the [newsgroup announcement](https://groups.google.com/forum/#!topic/mozilla.dev.platform/tezdW299Zds) for details.
