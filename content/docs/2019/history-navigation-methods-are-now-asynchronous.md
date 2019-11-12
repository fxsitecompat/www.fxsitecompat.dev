---
title: "History navigation methods are now asynchronous"
date: "2019-10-07T10:50:00-04:00"
categories: ["html"]
tags: []
versions: ["70"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1563587"
      title: "Bug 1563587 - Make history navigations asynchronous"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1594345"
      title: "Bug 1594345 - Close the Wikipedia's Image Viewer does jump page to top"
---
Starting with Firefox 70, the [`history.back`](https://developer.mozilla.org/docs/Web/API/History/back), [`history.forward`](https://developer.mozilla.org/docs/Web/API/History/forward) and [`history.go`](https://developer.mozilla.org/docs/Web/API/History/go) methods will behave asynchronously like Google Chrome and Apple Safari. This change may break any site relying on (browser detection and) the synchronous behaviour which can still be seen in Microsoft Edge, as pointed out in a [bug comment](https://bugzilla.mozilla.org/show_bug.cgi?id=1563587#c26). You can listen to the [`popstate`](https://developer.mozilla.org/docs/Web/API/Window/popstate_event) event to know when a history navigation is complete.

**Update**: This change is affecting *Wikipedia*.
