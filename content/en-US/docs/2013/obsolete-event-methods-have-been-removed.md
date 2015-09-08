---
title: "Obsolete event methods have been removed"
date: "2013-05-19T07:35:00-04:00"
categories: ["dom"]
tags: []
versions: "24"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=673919": "Bug 673919 – Remove routeEvent, enableExternalCapture and disableExternalCapture"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=874003": "Bug 874003 – Remove preventBubble and preventCapture"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=726933": "Bug 726933 – Warn about getPreventDefault being deprecated"
---
The [`routeEvent`](https://developer.mozilla.org/en-US/docs/Web/API/window.routeEvent), `enableExternalCapture`, and `disableExternalCapture` methods on the [`window`](https://developer.mozilla.org/en-US/docs/Web/API/window) object have been removed. They were non-standard Netscape-derived APIs [deprecated since Firefox 3](https://developer.mozilla.org/en-US/docs/Gecko_1.9_Changes_affecting_websites) and the implementation has been no-op (doing nothing). Meanwhile, [`captureEvents`](https://developer.mozilla.org/en-US/docs/Web/API/window.captureEvents) and [`releaseEvents`](https://developer.mozilla.org/en-US/docs/Web/API/window.releaseEvents) are kept for backward compatibility as Google's research revealed that many sites relied on those methods for feature detection.

The deprecated `preventBubble` and `preventCapture` methods, which were in the earlier W3C draft, have also been removed. The [`stopPropagation`](https://developer.mozilla.org/en-US/docs/Web/API/event.stopPropagation) method can be used instead.

Additionally, the non-standard `getPreventDefault` method, deprecated since Firefox 16, will be removed soon in favor of the [`defaultPrevented`](https://developer.mozilla.org/en-US/docs/Web/API/event.defaultPrevented) property. If `getPreventDefault` is used in a Web page, [Web Console](https://developer.mozilla.org/en-US/docs/Tools/Web_Console) shows a warning about the deprecation.
