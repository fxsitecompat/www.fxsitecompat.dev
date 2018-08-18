---
title: "`preventDefault()` on `keydown` now cancels `keypress`"
date: "2013-07-14T19:12:37-04:00"
categories: ["dom"]
tags: []
versions: ["25"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=501496"
      title: "Bug 501496 – preventDefault on keydown does not cancel following keypress"
---
Previously, calling the [`preventDefault`](https://developer.mozilla.org/docs/Web/API/event.preventDefault) method on a [`keydown`](https://developer.mozilla.org/docs/Web/Events/keydown) event didn't cancel the following [`keypress`](https://developer.mozilla.org/docs/Web/Events/keypress) event. It has been fixed to match the DOM Level 3 Events (D3E) spec as well as the behaviour of other browsers.
