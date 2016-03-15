---
title: "Some event attributes are now limited to `body` and `frameset`"
date: "2012-12-03T03:54:45-05:00"
categories: [event-handling]
tags: []
versions: ["19"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=809765"
      title: "Bug 809765 – Stop compiling the beforeunload attribute into an event handler on elements other than <body> and <frameset>"
---
Previously, the [`onbeforeunload`](https://developer.mozilla.org/en-US/docs/Web/API/window.onbeforeunload) attribute has been recognized even if it has been set on any elements, and the named handler is called when the event is fired. To comply with the spec, it's now ignored when it has been set on elements other than [`body`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/body) and [`<frameset>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/frameset). The other attributes treated the same include [`onafterprint`](https://developer.mozilla.org/en-US/docs/Web/API/window.onafterprint), [`onbeforeprint`](https://developer.mozilla.org/en-US/docs/Web/API/window.onbeforeprint), [`onhashchange`](https://developer.mozilla.org/en-US/docs/Web/API/window.onhashchange), [`onoffline`](https://developer.mozilla.org/en-US/docs/Web/API/window.onoffline), [`ononline`](https://developer.mozilla.org/en-US/docs/Web/API/window.ononline), [`onpagehide`](https://developer.mozilla.org/en-US/docs/Web/API/window.onpagehide), [`onpageshow`](https://developer.mozilla.org/en-US/docs/Web/API/window.onpageshow), [`onpopstate`](https://developer.mozilla.org/en-US/docs/Web/API/window.onpopstate), [`onresize`](https://developer.mozilla.org/en-US/docs/Web/API/window.onresize) and [`onunload`](https://developer.mozilla.org/en-US/docs/Web/API/window.onunload).
