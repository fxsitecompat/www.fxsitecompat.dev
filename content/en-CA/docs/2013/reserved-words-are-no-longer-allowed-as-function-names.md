---
title: "Reserved words are no longer allowed as function names"
date: "2013-09-19T23:58:13-04:00"
categories: ["javascript"]
tags: []
versions: ["26"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=907958"
      title: "Bug 907958 – Restrict function names to non-keywords"
---
The [reserved words](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Reserved_Words) cannot be used for function names. Starting with Firefox 26, such a usage will throw a [`SyntaxError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError). For example, `function delete() { ... }` is illegal.
