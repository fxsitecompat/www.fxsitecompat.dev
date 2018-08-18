---
title: "`getAttribute()` returns `null` for attributes created with `setAttributeNode` and containing upper-case characters in name"
date: "2015-10-22T22:14:00-07:00"
categories: ["dom"]
tags: []
versions: ["38"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1165851"
      title: "Bug 1165851 - document.createAttribute can not get their own Added attributes"
---
Firefox 38 has changed the implementation of the [`Element.setAttributeNode`](https://developer.mozilla.org/docs/Web/API/Element/setAttributeNode) method to align with the spec. As the side effect, the [`Element.getAttribute`](https://developer.mozilla.org/docs/Web/API/Element/getAttribute) method can no longer access attributes and returns `null`, if those are created with `setAttributeNode`, set with [`NamedNodeMap.setNamedItem`](https://developer.mozilla.org/docs/Web/API/NamedNodeMap/setNamedItem), and containing one or more upper-case characters in the attribute name. After breaking a couple of sites, this issue has been fixed with Firefox 39 by backing out the original change.
