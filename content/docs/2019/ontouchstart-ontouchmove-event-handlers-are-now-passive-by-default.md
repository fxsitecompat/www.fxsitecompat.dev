---
title: "`ontouchstart`, `ontouchmove` event handlers are now passive by default"
date: "2019-09-04T23:51:00-04:00"
categories: ["dom"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1574223"
      title: "Bug 1574223 - Consider treating document level ontouchmove as passive"
---
Starting with Firefox 70, event handlers set with the `ontouchstart` or `ontouchmove` property on `window`, `document`, `document.documentElement` or `document.body` will be treated as passive by default, which means the event cannot be cancelled with `preventDefault()` within the handler method.

[Firefox 61](https://www.fxsitecompat.dev/en-CA/docs/2018/touch-event-listeners-are-now-passive-by-default-making-scrolling-faster-on-mobile/) has already made the same change to event listeners set with `addEventListener()`, and this was an overlooked case of the scroll performance improvement on mobile.
