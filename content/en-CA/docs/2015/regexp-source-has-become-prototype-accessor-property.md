---
title: "`RegExp.source` has become prototype accessor property"
date: "2015-06-13T15:20:46-04:00"
categories: ["javascript"]
tags: []
versions: ["41"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1120169"
      title: "Bug 1120169 - Implement RegExp.prototype.{global, ignoreCase, multiline, source, sticky, unicode}"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1138325"
      title: "Bug 1138325 - Turning RegExp#source from an instance property into an accessor breaks ClojureScript apps"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1150297"
      title: "Bug 1150297 - Move source property to RegExp instance again."
---
The `source` property on the [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp) instance has been moved to the prototype accessors, so it's now the [`RegExp.prototype.source`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/source) property. This change was originally made to Firefox 38 [along with other properties](https://www.fxsitecompat.com/en-CA/docs/2015/regexp-global-ignorecase-multiline-and-sticky-properties-are-now-prototype-accessor-properties/) but has been backed out due to Web compatibility issues. If you are using [*ClojureScript*](https://github.com/clojure/clojurescript), you have to update the library to the latest version or your app may be broken on Firefox 41 and later.
