---
title: "`HTMLCanvasElement.getContext` no longer accepts non-object context attributes"
date: "2016-02-07T23:01:00-05:00"
categories: ["canvas-webgl"]
tags: []
versions: ["44"]
statuses: "reverted"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=645792": "Bug 645792 - Implement correct behavior for getContext() failures"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1215072": "Bug 1215072 - Assertion failure: !JS_IsExceptionPending(cx), at ./HTMLCanvasElementBinding.cpp:231"
---
As part of the standard compliant, the [`HTMLCanvasElement.getContext`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement/getContext) method now throws a `TypeError` if the second `contextAttributes` argument is not an `Object`, `null` nor `undefined`. See the MDN article for the possible attributes.

**Update**: This change has been [reverted with Firefox 45](https://bugzilla.mozilla.org/show_bug.cgi?id=1244480) since *Livecode* Emscripten code was broken due to the invalid `false` argument.
