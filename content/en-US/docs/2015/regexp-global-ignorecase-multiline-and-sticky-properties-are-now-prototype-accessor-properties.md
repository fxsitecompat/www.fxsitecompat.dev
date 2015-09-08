---
title: "`RegExp` `global`, `ignoreCase`, `multiline` and `sticky` properties are now prototype accessor properties"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
versions: "38"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1120169": "Bug 1120169 - Implement RegExp.prototype.{global, ignoreCase, multiline, source, sticky, unicode}"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1138325": "Bug 1138325 - Turning RegExp#source from an instance property into an accessor breaks ClojureScript apps"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1150297": "Bug 1150297 - Move source property to RegExp instance again."
---
The `global`, `ignoreCase`, `multiline` and `sticky` properties on the [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp) instance have been moved to the prototype accessors. Those are now [`RegExp.prototype.global`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Regexp/global), [`RegExp.prototype.ignoreCase`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Regexp/ignoreCase), [`RegExp.prototype.multiline`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Regexp/multiline), and [`RegExp.prototype.sticky`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Regexp/sticky). The change to the [`source`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Regexp/source) property is non-Release only due to Web compatibility issues.
