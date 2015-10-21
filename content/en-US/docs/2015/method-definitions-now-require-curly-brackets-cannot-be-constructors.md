---
title: "Method definitions now require curly brackets, cannot be constructors"
date: "2015-06-13T15:20:46-04:00"
categories: ["javascript"]
tags: []
versions: ["41"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1150855": "Bug 1150855 - Method definitions require curly brackets"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1059908": "Bug 1059908 - Method definitions and getter/setter functions should not be constructors"
---
Previously, curly brackets were not required in [method definitions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Method_definitions). Starting with Firefox 41, those are required as per the ECMAScript 6 specification and will throw a [`SyntaxError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError) if missing. At the same time, method definitions can no longer be constructors except for generator methods.
