---
title: "`Function.length` no longer counts default parameters"
date: "2013-01-03T03:53:26-05:00"
categories: ["javascript"]
tags: []
versions: ["18", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=777061"
      title: "Bug 777061 – Function .length property should not count rest parameters or parameters with default values"
---
The [`Function.length`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/length) property, indicating the number of arguments the function expects, has previously included [parameters with default values](https://developer.mozilla.org/docs/Web/JavaScript/Reference/default_parameters). This was fixed not to include those parameters. So `(function (a, b, c = false) {}).length` will be `2` instead of `3`.
