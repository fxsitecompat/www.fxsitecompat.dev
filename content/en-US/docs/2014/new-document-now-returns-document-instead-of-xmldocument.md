---
title: "`new Document()` now returns `Document` instead of `XMLDocument`"
date: "2014-06-09T02:46:54-04:00"
categories: ["dom"]
tags: []
versions: ["32"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1017932": "Bug 1017932 – Document() constructor should return Document object (not XMLDocument)"
---
The `Document` constructor starts returning a [`Document`](https://developer.mozilla.org/en-US/docs/Web/API/Document) object instead of [`XMLDocument`](https://developer.mozilla.org/en-US/docs/Web/API/XMLDocument) to follow the latest spec. They are identical except the [`load`](https://developer.mozilla.org/en-US/docs/Web/API/XMLDocument.load) method which is only available on `XMLDocument`. The [`DOMImplementation.createDocument`](https://developer.mozilla.org/en-US/docs/Web/API/DOMImplementation.createDocument) method continues returning an `XMLDocument` object.
