---
title: "`parseInt` now parses leading-zero strings as decimal, not octal"
date: "2013-02-06T08:44:10-05:00"
categories: ["javascript"]
tags: []
versions: "21"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=786135": "Bug 786135 – Make parseInt(\"042\") === 42, now that other engines are moving that way"
---
The [`parseInt`](https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Global_Objects/parseInt) method implementation has been updated to conform to the ECMAScript 5 spec, and it now parses leading-zero strings as decimal, not octal. Therefore, `parseInt("042")` will return `42` instead of `34`. If you'd like to parse strings as octal, specify the radix like `parseInt(str, 8)`.
