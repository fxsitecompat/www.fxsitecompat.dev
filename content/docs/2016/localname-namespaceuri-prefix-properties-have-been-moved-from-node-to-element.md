---
title: "`localName`, `namespaceURI`, `prefix` properties have been moved from `Node` to `Element`"
date: "2016-04-24T01:37:00-04:00"
categories: ["dom"]
tags: []
versions: ["48"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1055776"
      title: "Bug 1055776 - Investigate moving namespaceURI, prefix, and localName to Element and Attr"
---
The [`localName`](https://developer.mozilla.org/docs/Web/API/Element/localName), [`namespaceURI`](https://developer.mozilla.org/docs/Web/API/Node/namespaceURI) and [`prefix`](https://developer.mozilla.org/docs/Web/API/Node/prefix) properties on the [`Node`](https://developer.mozilla.org/docs/Web/API/Node) interface have been moved to the [`Element`](https://developer.mozilla.org/docs/Web/API/Element) and [`Attr`](https://developer.mozilla.org/docs/Web/API/Attr) interfaces, as per the recent DOM spec. All those properties will return `undefined` on other nodes. Chrome 48 has already made this change, so major compatibility issues are not expected.
