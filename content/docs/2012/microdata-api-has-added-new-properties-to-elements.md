---
title: "Microdata API has added new properties to elements"
date: "2012-10-15T06:00:00-04:00"
categories: ["dom"]
tags: []
versions: ["16"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=591467"
      title: "Bug 591467 – Implement HTML Microdata API"
---
The HTML5 [Microdata DOM API](https://www.w3.org/TR/microdata/#microdata-dom-api) has been implemented, adding the `getItems` property to the [`Document`](https://developer.mozilla.org/docs/Web/API/Document) interface as well as the `itemId`, `itemProp`, `itemRef`, `itemScope`, `itemType`, `itemValue` and `properties` properties to the [`Element`](https://developer.mozilla.org/docs/Web/API/Element) interface.

Six Apart's *Movable Type* is known to be affected by this change. They have [fixed the issue](https://github.com/movabletype/movabletype/commit/83d2f3d21d9c9a951d7e872d70bac5d355bd3d4d) and [issued a patch](https://movabletype.org/news/2012/10/patch_file_for_firefox_16.html) after some features were broken due to its custom `itemId` property.

If you'd like to add custom data to each element, it should be safer to use the [`HTMLElement.dataset`](https://developer.mozilla.org/docs/Web/API/HTMLElement/dataset) property rather than arbitrary properties. Firefox has also implemented the [`setUserData`](https://developer.mozilla.org/docs/Web/API/Node/setUserData) and [`getUserData`](https://developer.mozilla.org/docs/Web/API/Node/getUserData) methods that allow storing non-string data. However, those methods have been [deprecated](https://bugzilla.mozilla.org/show_bug.cgi?id=749981) in favour of the [`WeakMap`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) object.

**Update**: The Microdata API support has been [removed with Firefox 49](https://www.fxsitecompat.com/en-CA/docs/2016/microdata-api-has-been-removed/).
