---
title: "Touch event listeners are now `passive` by default, making scrolling faster on mobile"
date: "2018-04-25T18:02:00-04:00"
categories: ["dom"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1449268"
      title: "Bug 1449268 - Treat document-level touch event listeners as passive. (Chrome scrolling intervention)"
---
Starting with Firefox 61, `touchstart` and `touchmove` event listeners on `window`, `document` and `document.body` will be treated as `passive` by default, which means these events cannot be cancelled using [`preventDefault()`](https://developer.mozilla.org/en-US/docs/Web/API/Event/preventDefault) within the listeners unless you explicitly set [`addEventListener`](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)'s `passive` option `false`.

The scrolling intervention aims to improve touch scrolling performance on mobile devices as described in [this article on the Google Developers site](https://developers.google.com/web/updates/2017/01/scrolling-intervention). Given that Chrome 56 shipped in January 2017 has already adopted the new behaviour, the compatibility risk should be low.
