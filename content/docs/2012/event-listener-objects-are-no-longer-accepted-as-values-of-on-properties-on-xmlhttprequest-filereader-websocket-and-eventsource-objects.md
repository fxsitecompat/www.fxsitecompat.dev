---
title: "Event listener objects are no longer accepted as values of `on*` properties on `XMLHttpRequest`, `FileReader`, `WebSocket`, and `EventSource` objects"
date: "2012-12-29T03:53:26-05:00"
categories: ["dom"]
tags: []
versions: ["18"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=687332"
      title: "Bug 687332 – Move various onfoo event listeners off of DOM objects and into event listener managers"
---
With this change, handlers in the form of an object with a `handleEvent` property, e.g. `xhr.onreadystatechange = { handleEvent: function() { ... } }`, don't work anymore on [`XMLHttpRequest`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest), [`WebSocket`](https://developer.mozilla.org/docs/Web/API/WebSocket), [`FileReader`](https://developer.mozilla.org/docs/Web/API/FileReader) and [`EventSource`](https://developer.mozilla.org/docs/Web/API/EventSource) objects, just like the already didn't work on the [`element`](https://developer.mozilla.org/docs/Web/API/element), [`document`](https://developer.mozilla.org/docs/Web/API/document), and [`window`](https://developer.mozilla.org/docs/Web/API/window) objects. In Firefox (Gecko), such code will be treated as equivalent to `xhr.onreadystatechange = null`, thus it won't be executed while no error causes. This is a step to comply with standards and improve interoperability; it will be the same behaviour as Internet Explorer and Opera. WebKit browsers like Google Chrome still accept such forms.

Note that `xhr.onreadystatechange = function() { ... }` continues to work, though using [`addEventListener`](https://developer.mozilla.org/docs/Web/API/EventTarget.addEventListener) instead is generally recommended.
