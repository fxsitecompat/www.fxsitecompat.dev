---
title: "`HTMLIFrameElement.sandbox` now returns `DOMSettableTokenList`"
date: "2014-02-07T11:57:09-05:00"
categories: ["dom"]
tags: []
versions: "29"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=845057": "Bug 845057 – Fix the type of HTMLIFrameElement.sandbox"
---
Previously, the `sandbox` property of the [`HTMLIFrameElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLIFrameElement) interface (the [`<iframe>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe) element) returned a string value like `allow-same-origin`. This type has been changed to [`DOMSettableTokenList`](https://developer.mozilla.org/en-US/docs/Web/API/DOMSettableTokenList) to meet the latest spec. `sandbox.value` returns a string notation as before.
