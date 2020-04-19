---
title: "`cloneNode()` and `importNode()` has defaulted to shallow clones"
date: "2014-02-07T11:57:09-05:00"
categories: ["dom"]
tags: []
versions: ["29", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=937461"
      title: "Bug 937461 – Make cloneNode/importNode with the \"deep\" arg not passed default to shallow cloning"
---
The [`Node.cloneNode`](https://developer.mozilla.org/docs/Web/API/Node.cloneNode) and [`document.importNode`](https://developer.mozilla.org/docs/Web/API/document.importNode) methods take the boolean `deep` argument. It was optional in the DOM4 specification, and if omitted, these methods acted as if the value of `deep` was `true`. But this behaviour has been changed in the latest spec, and if omitted, the methods will act as if the value was `false`. The implementation has been changed in Firefox 29, and a shallow clone is now default instead of a deep clone. [Firefox 28](https://www.fxsitecompat.dev/en-CA/docs/2013/make-sure-the-deep-argument-is-specified-for-clonenode-and-importnode/) warned developers in console not to omit the argument both for the backward and forward compatibility.
