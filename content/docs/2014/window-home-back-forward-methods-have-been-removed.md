---
title: "`window.home`, `back`, `forward` methods have been removed"
date: "2014-04-03T19:31:02-04:00"
categories: ["dom"]
tags: []
versions: ["31", "31-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1012944"
      title: "Bug 1012944 – User login and account creation on deezer.com broken since Firefox 30.0b1, say home.display is not a function"
---
The non-standard, Netscape-derived [`window.home`](https://developer.mozilla.org/docs/Web/API/window/home), [`window.back`](https://developer.mozilla.org/docs/Web/API/window/back) and [`window.forward`](https://developer.mozilla.org/docs/Web/API/window/forward) methods have been removed. The standard [`history.back`](https://developer.mozilla.org/docs/Web/API/history/back) and [`history.forward`](https://developer.mozilla.org/docs/Web/API/history/forward) methods can be used instead to [manipulate the browser history](https://developer.mozilla.org/docs/Web/Guide/API/DOM/Manipulating_the_browser_history).
