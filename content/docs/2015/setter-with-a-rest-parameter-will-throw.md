---
title: "Setter with a rest parameter will throw"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
releases: ["38", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1089632"
      title: "Bug 1089632 – Setter with a RestParameter should be a SyntaxError"
---
A [setter](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/set) with a [rest parameter](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/rest_parameters) will throw a [`SyntaxError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError) exception as per the spec.
