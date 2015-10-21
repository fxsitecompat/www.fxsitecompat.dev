---
title: "When `undefined` is passed as an argument, the default parameter will be used if any"
date: "2013-01-03T03:53:26-05:00"
categories: ["javascript"]
tags: []
versions: ["18"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=781422": "Bug 781422 – parameters should get defaults whenever they are undefined"
---
The [default parameter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/default_parameters) is an ECMAScript 6 feature implemented Firefox 15. Previously, when [`undefined`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined) was passed as an argument, the value became `undefined`. The implementation has been changed to be the default value just like no argument was passed.
