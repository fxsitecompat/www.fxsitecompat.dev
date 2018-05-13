---
title: "`Element.getElementsBy*` now returns `HTMLCollection`"
date: "2012-12-03T03:54:45-05:00"
categories: ["dom"]
tags: []
versions: ["19"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=799464"
      title: "Bug 799464 – Make Element.getElementsBy* return HTMLCollection"
---
The type of element lists that can be retrieved with the [`getElementsByTagName`](https://developer.mozilla.org/docs/Web/API/element.getElementsByTagName), [`getElementsByTagNameNS`](https://developer.mozilla.org/docs/Web/API/element.getElementsByTagNameNS) and [`getElementsByClassName`](https://developer.mozilla.org/docs/Web/API/element.getElementsByClassName) methods have been changed from [`NodeList`](https://developer.mozilla.org/docs/Web/API/NodeList), defined in the DOM3 Core spec, to [`HTMLCollection`](https://developer.mozilla.org/docs/Web/API/HTMLCollection), defined in the DOM4 spec draft.
