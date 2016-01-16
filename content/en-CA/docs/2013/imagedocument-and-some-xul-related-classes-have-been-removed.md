---
title: "`ImageDocument` and some XUL-related classes have been removed"
date: "2013-07-14T19:12:37-04:00"
categories: ["dom"]
tags: []
versions: ["25"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=885177": "Bug 885177 – Make window.ImageDocument ChromeOnly"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=898687": "Bug 898687 – Remove XULTreeBuilder from content"
---
The non-standard `ImageDocument` interface, as well as the `BoxObject`, `TreeColumn`, `TreeColumns`, `TreeContentView`, `TreeSelection`, `XULControllers`, `XULTemplateBuilder` and `XULTreeBuilder` interfaces are no longer available from Web content.
