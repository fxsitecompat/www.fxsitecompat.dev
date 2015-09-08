---
title: "Global variables with the same name as `window` properties now call the property setter when they are set"
date: "2014-04-03T19:31:02-04:00"
categories: ["dom"]
tags: []
versions: "31"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=932322": "Bug 932322 – Make Window\'s WebIDL properties be own properties of window"
---
A typical impact of this change has been reported as [Bug 943958](https://bugzilla.mozilla.org/show_bug.cgi?id=943958). Code like `var name = 1` no longer works as expected, instead `name` will return a string `"1"` because of the [`window.name`](https://developer.mozilla.org/en-US/docs/Web/API/window/name) property. This will be the same behavior as WebKit and Blink. Web developers should always avoid using global variables with the same name as [`window`](https://developer.mozilla.org/en-US/docs/Web/API/window) properties.
