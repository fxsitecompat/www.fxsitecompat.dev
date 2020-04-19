---
title: "`HTMLElement` members are no more available on the whole inheritage chain"
date: "2012-12-29T08:29:30-05:00"
categories: ["dom"]
tags: []
releases: ["20", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=821606"
      title: "Bug 821606 – Turn on WebIDL bindings for Element and HTMLElement"
---
Where we used to have all members of the entire inheritance chain (e.g. [`HTMLDivElement`](https://developer.mozilla.org/docs/Web/API/HTMLDivElement) → [`HTMLElement`](https://developer.mozilla.org/docs/Web/API/HTMLElement) → [`Element`](https://developer.mozilla.org/docs/Web/API/Element) → [`Node`](https://developer.mozilla.org/docs/Web/API/Node) → [`EventTarget`](https://developer.mozilla.org/docs/Web/API/EventTarget)) on the interface prototype object of the leaf class (e.g. `HTMLDivElement.prototype === document.createElement("div").__proto`), we now put the members of [`HTMLElement`](https://developer.mozilla.org/docs/Web/API/HTMLElement) just on `HTMLElement.prototype` (`=== HTMLDivElement.prototype.__proto__`).

It turns out that at least one important library, [Optimizely](https://www.optimizely.com/), relied on this erroneous behaviour. They quickly fixed it on their side, but it is important that any Web site using their tool upgrade to the latest versions.

Passing [`null`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/null) to a method that takes a [`DOMString`](https://developer.mozilla.org/docs/Web/API/DOMString) argument will stringify to `"null"` instead of the empty string. For example, `element.setAttribute("foo", null)` will result in an output like `<div foo="null">` instead of `<div foo="">`.

The `parseFromStream` and `parseFromBuffer` methods of [`DOMParser`](https://developer.mozilla.org/docs/Web/API/DOMParser) as well as the `serializeToStream` method of [`XMLSerializer`](https://developer.mozilla.org/docs/Web/API/XMLSerializer) are now deprecated and no longer available on content. Those still work on chrome (or extension code).
