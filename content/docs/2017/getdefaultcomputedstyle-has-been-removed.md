---
title: "`getDefaultComputedStyle()` has been removed"
date: "2017-04-16T03:00:00-04:00"
categories: ["dom"]
tags: []
versions: ["55"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1355683"
      title: "Bug 1355683 - Consider removing getDefaultComputedStyle"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/dGDkR65Ffa4/discussion"
      title: "Intent to unship: Window.getDefaultComputedStyle"
---
The non-standard [`window.getDefaultComputedStyle`](https://developer.mozilla.org/en-US/docs/Web/API/Window/getDefaultComputedStyle) method, that returns the browser's default computed values on an element, has been removed with Firefox 55. Unlike the similar [`getComputedStyle`](https://developer.mozilla.org/en-US/docs/Web/API/Window/getComputedStyle) method, it has never been standardized as part of the CSSOM spec nor implemented in other browsers.

It's known to be used in jQuery, but the removal should not be a problem thanks to proper feature detection and fallback. No other use cases have been identified.

**Update**: Due to a [compatibility issue](https://bugzilla.mozilla.org/show_bug.cgi?id=548397) affecting the older versions of jQuery, where `getComputedStyle` returns `null` inside invisible iframes, this change has been backed out from Firefox 55. However, the `getDefaultComputedStyle` method will be removed anyway in the future.
