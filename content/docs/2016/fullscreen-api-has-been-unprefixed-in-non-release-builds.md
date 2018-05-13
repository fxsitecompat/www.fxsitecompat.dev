---
title: "Fullscreen API has been unprefixed in non-release builds"
date: "2016-02-17T09:21:00-05:00"
categories: ["dom"]
tags: []
versions: ["47"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=743198"
      title: "Bug 743198 - Unprefix the DOM fullscreen API"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1249225"
      title: "Bug 1249225 - Remove the prefixed fullscreen API"
aliases:
    - "/en-CA/docs/2016/fullscreen-api-has-been-unprefixed/"
---
The [Fullscreen API](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) has been unprefixed with Firefox 47. The non-standard, prefixed methods and properties are now considered deprecated and may be removed in the future.

The `element.mozRequestFullScreen` and [`document.mozCancelFullScreen`](https://developer.mozilla.org/docs/Web/API/Document/mozCancelFullScreen) methods are now [`element.requestFullscreen`](https://developer.mozilla.org/docs/Web/API/Element/requestFullScreen) and `document.exitFullscreen` respectively.

The [`document.mozFullScreenEnabled`](https://developer.mozilla.org/docs/Web/API/Document/mozFullScreenEnabled) and [`document.mozFullScreenElement`](https://developer.mozilla.org/docs/Web/API/Document/mozFullScreenElement) properties are now `document.fullscreenEnabled` and `document.fullscreenElement` respectively.

The [`document.mozFullScreen`](https://developer.mozilla.org/docs/Web/API/Document/mozFullScreen) property has no exact standard equivalent. Use `document.fullscreenElement` instead.

The `mozfullscreenchange` and `mozfullscreenerror` events are now [`fullscreenchange`](https://developer.mozilla.org/docs/Web/Events/fullscreenchange) and [`fullscreenerror`](https://developer.mozilla.org/docs/Web/Events/fullscreenerror) respectively.

**Update**: Due to several site compatibility issues, the unprefixed API has been [disabled](https://bugzilla.mozilla.org/show_bug.cgi?id=1268749) in the Beta and Release channels and will be [re-enabled](https://bugzilla.mozilla.org/show_bug.cgi?id=1269276) in the future. We have updated this document's title accordingly. The unprefixed API remains enabled in the Nightly and Aurora (Developer Edition) channels so that Web developers can test their sites. Note that there is a [proposal](https://bugzilla.mozilla.org/show_bug.cgi?id=1269157) to implement `document.fullscreen` as the unprefixed version of `document.mozFullScreen` to make the transition easier.
