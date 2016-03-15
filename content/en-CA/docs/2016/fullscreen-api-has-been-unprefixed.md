---
title: "Fullscreen API has been unprefixed"
date: "2016-02-17T09:21:00-05:00"
categories: ["dom"]
tags: []
versions: ["47"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=743198"
      title: "Bug 743198 - Unprefix the DOM fullscreen API"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1249225"
      title: "Bug 1249225 - Remove the prefixed fullscreen API"
---
The [Fullscreen API](https://developer.mozilla.org/en-US/docs/Web/API/Fullscreen_API) has been unprefixed with Firefox 47. The non-standard, prefixed methods and properties are now considered deprecated and may be removed in the future.

The `element.mozRequestFullScreen` and [`document.mozCancelFullScreen`](https://developer.mozilla.org/en-US/docs/Web/API/Document/mozCancelFullScreen) methods are now [`element.requestFullscreen`](https://developer.mozilla.org/en-US/docs/Web/API/Element/requestFullScreen) and `document.exitFullscreen` respectively.

The [`document.mozFullScreenEnabled`](https://developer.mozilla.org/en-US/docs/Web/API/Document/mozFullScreenEnabled) and [`document.mozFullScreenElement`](https://developer.mozilla.org/en-US/docs/Web/API/Document/mozFullScreenElement) properties are now `document.fullscreenEnabled` and `document.fullscreenElement` respectively.

The [`document.mozFullScreen`](https://developer.mozilla.org/en-US/docs/Web/API/Document/mozFullScreen) property has no exact standard equivalent. Use `document.fullscreenElement` instead.
