---
title: "`RegExp.source` has become prototype accessor property"
date: "2015-06-13T15:20:46-04:00"
categories: ["javascript"]
tags: []
versions: "41"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1120169": "Bug 1120169 - Implement RegExp.prototype.{global, ignoreCase, multiline, source, sticky, unicode}"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1138325": "Bug 1138325 - Turning RegExp#source from an instance property into an accessor breaks ClojureScript apps"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1150297": "Bug 1150297 - Move source property to RegExp instance again."
---
The `source` property on the [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp) instance has been moved to the prototype accessors, so it's now the [`RegExp.prototype.source`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/source) property. This change was originally made to [Firefox 38](https://www.fxsitecompat.com/en-US/versions/38/) along with other properties but has been backed out due to Web compatibility issues. If you are using [ClojureScript](https://github.com/clojure/clojurescript), you have to update the library to the latest version or your app may be broken on Firefox 41 and later.
