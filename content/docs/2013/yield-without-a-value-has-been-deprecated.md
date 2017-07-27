---
title: "`yield` without a value has been deprecated"
date: "2013-07-14T19:12:37-04:00"
categories: ["javascript"]
tags: []
versions: ["25"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=885463"
      title: "Bug 885463 – Warn about \'yield\' without operand"
---
The [`yield`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/yield) operator now cannot be used without an operand (its value). This change has been made to comply with the [ECMAScript 6](https://developer.mozilla.org/en-US/docs/JavaScript/ECMAScript_6_support_in_Mozilla) spec, and you'll see a warning in the [Web Console](https://developer.mozilla.org/en-US/docs/Tools/Web_Console) if no value is specified in your code. You can just use `yield undefined` instead if there's no specific value to return.
