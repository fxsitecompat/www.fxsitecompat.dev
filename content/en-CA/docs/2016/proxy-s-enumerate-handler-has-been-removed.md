---
title: "`Proxy`'s `enumerate` handler has been removed"
date: "2016-02-14T03:53:00-05:00"
categories: ["javascript"]
tags: []
versions: ["47"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1246318": "Bug 1246318 - Remove [[Enumerate]] and associated reflective capabilities"
---
The [`handler.enumerate`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy/handler/enumerate) method, used in [`Proxy`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy) to trap [`for-in`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in) statements, has been removed from the ECMAScript 2016 (ES7) spec and Firefox 47.
