---
title: "Code in `eval` doesn\'t work when the Debugger is activated"
date: "2014-03-21T04:50:04-04:00"
categories: ["javascript"]
tags: []
versions: "30"
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=998908": "Bug 998908 – [jsdbg2] Calling Debugger.Script.prototype.getChildScripts causes errors to be thrown that otherwise wouldn\'t be"
---
Due to a regression in the JavaScript engine, a part of script inside an [`eval`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/eval) may not work properly and throw a `ReferenceError` while the [Debugger](https://developer.mozilla.org/en-US/docs/Tools/Debugger) or the [Firebug](https://getfirebug.com/) extension is activated on Firefox. Use [Firefox Aurora or Beta](http://www.mozilla.org/en-US/firefox/channel/) to workaround this issue affecting ExtJS and Google Maps API in particular.
