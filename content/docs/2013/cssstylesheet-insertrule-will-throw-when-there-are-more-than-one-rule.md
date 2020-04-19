---
title: "`CSSStyleSheet.insertRule()` will throw when there are more than one rule"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
releases: ["21", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=765599"
      title: "Bug 765599 – CSSStyleSheet.insertRule should throw when there are more than one rule"
---
If multiple rules was passed to the [`CSSStyleSheet.insertRule`](https://developer.mozilla.org/docs/Web/API/CSSStyleSheet/insertRule) method, only the first rule was inserted into the stylesheet. Instead, Firefox now throws an exception `SYNTAX_ERR` like other browsers.
