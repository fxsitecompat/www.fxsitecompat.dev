---
title: "`getElementsByTagName` now matches `localName` instead of `tagName`"
date: "2015-10-23T02:32:00-07:00"
categories: ["dom"]
tags: []
versions: ["44"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=492933": "Bug 492933 - getElementsByTagName should match on localName not tagName (for interop)"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1236329": "Bug 1236329 - Error on HP Deskjet 2540 printer configuration page"
---
The [`Document.getElementsByTagName`](https://developer.mozilla.org/en-US/docs/Web/API/document/getElementsByTagName) and [`Element.getElementsByTagName`](https://developer.mozilla.org/en-US/docs/Web/API/Element/getElementsByTagName) methods are now matching the [`localName`](https://developer.mozilla.org/en-US/docs/Web/API/Node/localName) property of nodes instead of the [`tagName`](https://developer.mozilla.org/en-US/docs/Web/API/Element/tagName) property, as per the latest spec.

This change affects nodes with an XML namespace prefix, such as `<svg:circle>`. In this case, `getElementsByTagName('svg:circle')` no longer matches the node and  `getElementsByTagName('circle')` can be used instead. However, the [`getElementsByTagNameNS`](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementsByTagNameNS) method is more formal and recommended, therefore it could be replaced with `getElementsByTagNameNS('http://www.w3.org/2000/svg', 'circle')`.

Apparently the configuration page of some *HP* printers is broken due to this change.
