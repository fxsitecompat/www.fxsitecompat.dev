---
title: "Iterable objects now have `Symbol.iterator` instead of `\"@@iterator\"`"
date: "2014-12-19T11:15:21-05:00"
categories: ["javascript"]
tags: []
versions: ["36"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=918828": "Bug 918828 – Use @@iterator symbol instead of placeholder string"
---
The `"@@iterator"` property on [iterable objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/The_Iterator_protocol), including [`Array`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array), [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) and [`NodeList`](https://developer.mozilla.org/en-US/docs/Web/API/NodeList), has been replaced with the [`Symbol.iterator`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/iterator) property as defined in the ECMAScript 6 draft.
