---
title: "Make sure the `deep` argument is specified for `cloneNode()` and `importNode()`"
date: "2013-12-09T02:32:17-05:00"
categories: ["dom"]
tags: []
versions: ["28"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=937465"
      title: "Bug 937465 – Add a warning when cloneNode/importNode is used without a boolean argument on a node with children"
---
The [`Node.cloneNode`](https://developer.mozilla.org/docs/Web/API/Node.cloneNode) and [`document.importNode`](https://developer.mozilla.org/docs/Web/API/document.importNode) methods take the boolean `deep` argument. It's optional in the DOM4 specification, and if omitted, these methods acted as if the value of `deep` was `true`. But this behaviour has been changed in the latest spec, and if omitted, the methods will act as if the value was `false`. The implementation has been [changed in Firefox 29](https://www.fxsitecompat.com/en-CA/docs/2014/clonenode-and-importnode-has-defaulted-to-shallow-clones/). Though the argument is still optional, Firefox now warns developers in console not to omit the argument for the backward and forward compatibility.
