---
title: "Scroll-linked positioning effects may not work well with async scrolling, console warns"
date: "2016-01-07T09:01:00-05:00"
categories: ["javascript"]
tags: []
versions: ["46"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1229052": "Bug 1229052 - Log a warning if webpage is updating positioning properties during a scroll event listener"
aliases:
---
Starting with Firefox 46, the Web Console warns page scripts altering scroll positioning properties in a [`scroll`](https://developer.mozilla.org/en-US/docs/Web/Events/scroll) event listener. Such event handlers are often used for sticky element positioning, scroll snapping or parallax effects, but may not work well with asynchronous scrolling being implemented in Firefox. See the [Scroll-Linked Effects](https://developer.mozilla.org/en-US/docs/Mozilla/Performance/ScrollLinkedEffects) page on MDN for details and possible workarounds.
