---
title: "`ImageDocument` and some XUL-related classes have been removed"
date: "2013-07-14T19:12:37-04:00"
categories: ["dom"]
tags: []
versions: ["25", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=885177"
      title: "Bug 885177 – Make window.ImageDocument ChromeOnly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=898687"
      title: "Bug 898687 – Remove XULTreeBuilder from content"
---
The non-standard `ImageDocument` interface, as well as the `BoxObject`, `TreeColumn`, `TreeColumns`, `TreeContentView`, `TreeSelection`, `XULControllers`, `XULTemplateBuilder` and `XULTreeBuilder` interfaces are no longer available from Web content.
