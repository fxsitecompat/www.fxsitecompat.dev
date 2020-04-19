---
title: "Iterable objects now have `Symbol.iterator` instead of `\"@@iterator\"`"
date: "2014-12-19T11:15:21-05:00"
categories: ["javascript"]
tags: []
releases: ["36", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=918828"
      title: "Bug 918828 – Use @@iterator symbol instead of placeholder string"
---
The `"@@iterator"` property on [iterable objects](https://developer.mozilla.org/docs/Web/JavaScript/Guide/The_Iterator_protocol), including [`Array`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array), [`Map`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Map) and [`NodeList`](https://developer.mozilla.org/docs/Web/API/NodeList), has been replaced with the [`Symbol.iterator`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Symbol/iterator) property as defined in the ECMAScript 6 draft.
