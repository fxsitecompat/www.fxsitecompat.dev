---
title: "Use of sync XHR during `unload`, `pagehide` events is now deprecated"
date: "2019-06-09T03:55:00-04:00"
categories: ["dom"]
tags: []
versions: ["68"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=980902"
      title: "Bug 980902 - Warn about use of sync XHR during unload and pagehide events"
---
Starting with Firefox 68, Web Console warns when a synchronous `XMLHttpRequest` is used in an `unload` or `pagehide` event listener, because it contributes to negative user experience. You can use the [`navigator.sendBeacon`](https://developer.mozilla.org/docs/Web/API/Navigator/sendBeacon) method instead, which is now available in all modern browsers.

Note that use of synchronous `XMLHttpRequest` outside of these events has been warned since [Firefox 30](https://www.fxsitecompat.dev/en-CA/docs/2014/synchronous-xmlhttprequest-has-been-deprecated/). You may want to double-check your code to make sure all requests on the main thread are asynchronous.
