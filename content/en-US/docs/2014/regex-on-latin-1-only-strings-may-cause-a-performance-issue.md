---
title: "Regex on Latin-1-only strings may cause a performance issue"
date: "2014-07-22T05:06:26-04:00"
categories: ["javascript"]
tags: ["regression"]
versions: "33"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1081175": "Bug 1081175 – (latin1strings) Degraded regular expression performance (infinite loop?)"
---
In Firefox 33, regular expression operations on strings represented only as Latin-1 characters could be very slow, sometimes leading to a hang. This regression, due to an [internal character encoding change](https://blog.mozilla.org/javascript/2014/07/21/slimmer-and-faster-javascript-strings-in-firefox/), will be fixed with Firefox 34.
