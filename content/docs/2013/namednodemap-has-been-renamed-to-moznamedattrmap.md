---
title: "`NamedNodeMap` has been renamed to `MozNamedAttrMap`"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
versions: ["22"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=847195"
      title: "Bug 847195 – Make NamedNodeMap only deal with Attrs"
---
The [`NamedNodeMap`](https://developer.mozilla.org/docs/Web/API/NamedNodeMap) interface has been renamed to prefixed `MozNamedAttrMap`, as it has been removed from the spec and only available for [`Node.attributes`](https://developer.mozilla.org/docs/Web/API/Node.attributes).
