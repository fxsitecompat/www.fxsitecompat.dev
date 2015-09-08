---
title: "`delete` now triggers \"temporal dead zone\""
date: "2014-12-19T11:15:21-05:00"
categories: ["javascript"]
tags: []
versions: "36"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1074571": "Bug 1074571 – The delete operator should trigger TDZ"
---
The concept of the "[temporal dead zone](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let#Temporal_dead_zone_and_errors_with_let)", defined in ECMAScript 6 for the [`const`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/const) and [`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) statements, has been applied to the [`delete`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/delete) operator as well. As described in the document, if this operator is used in a function, a variable with the same name cannot be redeclared afterward, but rather it raises a [`ReferenceError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/ReferenceError).
