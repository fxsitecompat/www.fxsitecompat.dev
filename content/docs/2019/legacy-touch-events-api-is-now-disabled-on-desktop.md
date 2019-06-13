---
title: "Legacy Touch Events API is now disabled on desktop"
date: "2019-05-12T23:43:00-04:00"
categories: ["dom"]
tags: []
versions: ["67"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1412485"
      title: "Bug 1412485 - Consider removing some parts of touch event APIs on desktop"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1500631"
      title: "Bug 1500631 - Consider removing document.createTouch and document.createTouchList"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/dwRNENReBuU/discussion"
      title: "Disabling document.createEvent(\"TouchEvent\"), document.createTouch* and ontouch* event handlers on desktop"
---
Firefox 67 has followed [Chrome 70](https://www.chromestatus.com/feature/4764225348042752) to disable the legacy Touch Events API on desktop platforms, which had been available since [Firefox 52](https://www.fxsitecompat.dev/en-CA/docs/2016/touch-event-support-has-been-re-enabled-on-windows-desktop/), because websites keep misusing the API for mobile detection, treating Firefox as a mobile browser on desktop and laptop computers with a touchscreen.

These are no longer available on desktop:

* `createTouch`, `createTouchList`, `createEvent('TouchEvent')` methods on `document`
* `ontouchstart`, `ontouchmove`, `ontouchend`, `ontouchcancel` properties on `window`, `document`, `element`

The Touch Events API itself is still available on computers with a touchscreen, including:

* `Touch`, `TouchEvent`, `TouchList` interfaces on `window`
* `touchstart`, `touchmove`, `touchend`, `touchcancel` event handlers that can be used with `addEventListener()`

Note that the `createTouch` and `createTouchList` methods have been deprecated and will be completely removed from Firefox in the near future.
