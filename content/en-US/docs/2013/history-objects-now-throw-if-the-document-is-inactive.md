---
title: "`History` objects now throw if the `document` is inactive"
date: "2013-12-09T02:32:17-05:00"
categories: ["dom"]
tags: []
versions: "28"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=940783": "Bug 940783 – History objects should unconditionally throw if their inner is not current"
---
The spec of the [`History`](https://developer.mozilla.org/en-US/docs/Web/API/History) interface has been updated, and the properties and methods now throw a `SecurityError` exception when those are called on an inactive [`document`](https://developer.mozilla.org/en-US/docs/Web/API/document). It would be a problem if you are manipulating [`window.history`](https://developer.mozilla.org/en-US/docs/Web/API/window.history) in an [`<iframe>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe).
