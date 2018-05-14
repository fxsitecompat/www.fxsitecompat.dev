---
title: "`watch()` throws a `TypeError` on some interfaces"
date: "2013-04-06T04:52:59-04:00"
categories: ["dom"]
tags: []
versions: ["23"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=903332"
      title: "Bug 903332 – document.watch() results in \"TypeError: can\'t watch non-native objects of class Proxy\""
---
Since Firefox 23, the non-standard [`watch`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/watch) method, which allows developers to observe changes made to object properties, throws a [`TypeError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/TypeError) if the object is [`Document`](https://developer.mozilla.org/docs/Web/API/Document), [`HTMLSelectElement`](https://developer.mozilla.org/docs/Web/API/HTMLSelectElement) or probably some other DOM element interfaces. A workaround is to use a [`Proxy`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy). Note that `watch` and [`unwatch`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/unwatch) may be removed in the future, and you should avoid using those Firefox-specific methods. This regression has been fixed with Firefox 27.
