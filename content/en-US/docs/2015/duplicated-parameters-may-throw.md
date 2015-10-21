---
title: "Duplicated parameters may throw"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
versions: ["38"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1096376": "Bug 1096376 – Don\'t allow duplicate parameter names when rest-parameter is present"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1096377": "Bug 1096377 – Don\'t allow duplicate parameter names in arrow functions"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1096378": "Bug 1096378 – Don\'t allow duplicate parameter names in concise method definitions"
---
Starting with Firefox 38, duplicated function parameter names will throw a [`SyntaxError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError) exception when those are used with a [rest parameter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters), for a [arrow function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions), or for a concise method definition.
