---
title: "`cloneNode` and `importNode` has defaulted to shallow clones"
date: "2014-02-07T11:57:09-05:00"
categories: ["dom"]
tags: []
versions: "29"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=937461": "Bug 937461 – Make cloneNode/importNode with the \"deep\" arg not passed default to shallow cloning"
---
The [`Node.cloneNode`](https://developer.mozilla.org/en-US/docs/Web/API/Node.cloneNode) and [`document.importNode`](https://developer.mozilla.org/en-US/docs/Web/API/document.importNode) methods take the boolean `deep` argument. It was optional in the DOM4 specification, and if omitted, these methods acted as if the value of `deep` was `true`. But this behavior has been changed in the latest spec, and if omitted, the methods will act as if the value was `false`. The implementation has been changed in Firefox 29, and a shallow clone is now default instead of a deep clone. [Firefox 28](https://www.fxsitecompat.com/en-US/versions/28/) warned developers in console not to omit the argument both for the backward and forward compatibility.
