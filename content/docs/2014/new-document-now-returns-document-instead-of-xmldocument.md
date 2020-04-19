---
title: "`new Document()` now returns `Document` instead of `XMLDocument`"
date: "2014-06-09T02:46:54-04:00"
categories: ["dom"]
tags: []
releases: ["32", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1017932"
      title: "Bug 1017932 – Document() constructor should return Document object (not XMLDocument)"
---
The `Document` constructor starts returning a [`Document`](https://developer.mozilla.org/docs/Web/API/Document) object instead of [`XMLDocument`](https://developer.mozilla.org/docs/Web/API/XMLDocument) to follow the latest spec. They are identical except the [`load`](https://developer.mozilla.org/docs/Web/API/XMLDocument.load) method which is only available on `XMLDocument`. The [`DOMImplementation.createDocument`](https://developer.mozilla.org/docs/Web/API/DOMImplementation.createDocument) method continues returning an `XMLDocument` object.
