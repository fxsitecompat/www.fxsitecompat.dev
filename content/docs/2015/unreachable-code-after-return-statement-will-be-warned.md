---
title: "Unreachable code after `return` statement will be warned"
date: "2015-04-27T13:17:23-04:00"
categories: ["javascript"]
tags: []
versions: ["40", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1005110"
      title: "Bug 1005110 - Warn about unreachable code after semicolon-less return statement"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1151931"
      title: "Bug 1151931 - Warning for \"unreachable expression after semicolon-less return statement\" triggers incorrectly (braceless if, ASI)"
---
The [Web Console](https://developer.mozilla.org/docs/Tools/Web_Console) now shows a warning for a unreachable code after [`return`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/return) statement. This includes common misleading coding style: the [return statement followed by a line break](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/return#Automatic_semicolon_insertion) and some value meant to return.
