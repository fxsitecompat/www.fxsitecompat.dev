---
title: "`CSSStyleSheet.insertRule` will throw when there are more than one rule"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
versions: ["21"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=765599": "Bug 765599 – CSSStyleSheet.insertRule should throw when there are more than one rule"
---
If multiple rules was passed to the [`CSSStyleSheet.insertRule`](https://developer.mozilla.org/en-US/docs/Web/API/CSSStyleSheet/insertRule) method, only the first rule was inserted into the stylesheet. Instead, Firefox now throws an exception `SYNTAX_ERR` like other browsers.
