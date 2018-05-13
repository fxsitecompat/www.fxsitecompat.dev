---
title: "`scrollX`, `scrollY`, `pageXOffset`, `pageYOffset` now return double instead of integer"
date: "2017-03-18T22:09:00-04:00"
categories: ["dom"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1151421"
      title: "Bug 1151421 - Make window.pageYOffset/pageXOffset/scrollX/scrollY double, not integers"
---
On Firefox 55 and later, the [`scrollX`](https://developer.mozilla.org/docs/Web/API/Window/scrollX) and [`scrollY`](https://developer.mozilla.org/docs/Web/API/Window/scrollY) properties and those aliases [`pageXOffset`](https://developer.mozilla.org/docs/Web/API/Window/pageXOffset) and [`pageYOffset`](https://developer.mozilla.org/docs/Web/API/Window/pageYOffset) on `window` will return a double with sub-pixel precision, just like values returned by the [`getBoundingClientRect`](https://developer.mozilla.org/docs/Web/API/Element/getBoundingClientRect) method. If necessary, use the [`Math.round`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/round) method to cast those to traditional integer values.
