---
title: "`RegExp().source` now returns `\"(?:)\"` for empty regular expressions"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
versions: ["38", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1130798"
      title: "Bug 1130798 – new RegExp().source should return \"(?:)\""
---
The [`RegExp.prototype.source`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp/source) property now returns `"(?:)"` instead of an empty string for empty regular expressions, to match the spec.
