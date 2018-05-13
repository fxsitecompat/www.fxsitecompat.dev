---
title: "`RegExp` `global`, `ignoreCase`, `multiline` and `sticky` properties are now prototype accessor properties"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
versions: ["38"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1120169"
      title: "Bug 1120169 - Implement RegExp.prototype.{global, ignoreCase, multiline, source, sticky, unicode}"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1138325"
      title: "Bug 1138325 - Turning RegExp#source from an instance property into an accessor breaks ClojureScript apps"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1150297"
      title: "Bug 1150297 - Move source property to RegExp instance again."
---
The `global`, `ignoreCase`, `multiline` and `sticky` properties on the [`RegExp`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp) instance have been moved to the prototype accessors. Those are now [`RegExp.prototype.global`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Regexp/global), [`RegExp.prototype.ignoreCase`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Regexp/ignoreCase), [`RegExp.prototype.multiline`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Regexp/multiline), and [`RegExp.prototype.sticky`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Regexp/sticky). The change to the [`source`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Regexp/source) property has been [postponed to Firefox 41](https://www.fxsitecompat.com/en-CA/docs/2015/regexp-source-has-become-prototype-accessor-property/) due to Web compatibility issues.
