---
title: "Fullscreen API has been unprefixed"
date: "2018-09-23T00:24:00-04:00"
categories: ["dom"]
tags: []
versions: ["64"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1188256"
      title: "Bug 1188256 - Make Element.requestFullscreen() return a promise"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1269276"
      title: "Bug 1269276 - Enable unprefixed Fullscreen API by default for release versions"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1375319"
      title: "Bug 1375319 - Dispatch fullscreen events to element first rather than dispatch to document directly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1491212"
      title: "Bug 1491212 - Make Document.exitFullscreen() return a promise"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1492005"
      title: "Bug 1492005 - Deprecate prefixed Fullscreen API"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/uizXjqHDmQ8/discussion"
      title: "Intent to ship: Unprefixed Fullscreen API"
---
The unprefixed [Fullscreen API](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) has been finally enabled by default in Firefox 64 on all the channels, after years of efforts to improve the cross-browser compatibility. The last unprefix attempt was made back in [Firefox 47](https://www.fxsitecompat.com/en-CA/docs/2016/fullscreen-api-has-been-unprefixed-in-non-release-builds/), which was soon cancelled except for the Nightly channel. The `moz`-prefixed API is now considered deprecated and will be removed in the future.

[Google Chrome 71](https://groups.google.com/a/chromium.org/d/topic/blink-dev/ODzbWn-xRrQ/discussion) is also shipping the unprefixed API in December 2018, almost at the same time as the Firefox 64 release.

**Methods**: These methods now return a `Promise`.

| Prefixed | Standard |
| --- | --- |
| `Document.mozCancelFullScreen()` | [`Document.exitFullscreen()`](https://developer.mozilla.org/docs/Web/API/Document/exitFullscreen) |
| `Element.mozRequestFullScreen()` | [`Element.requestFullscreen()`](https://developer.mozilla.org/docs/Web/API/Element/requestFullScreen) |

**Properties**:

| Prefixed | Standard |
| --- | --- |
| `Document.mozFullScreen` | [`Document.fullscreen`](https://developer.mozilla.org/docs/Web/API/Document/fullscreen) |
| `Document.mozFullScreenElement` | [`Document.fullscreenElement`](https://developer.mozilla.org/docs/Web/API/DocumentOrShadowRoot/fullscreenElement) |
| `Document.mozFullScreenEnabled` | [`Document.fullscreenEnabled`](https://developer.mozilla.org/docs/Web/API/Document/fullscreenEnabled) |
| `Document.onmozfullscreenchange` | [`Document.onfullscreenchange`](https://developer.mozilla.org/docs/Web/API/Document/onfullscreenchange) |
| `Document.onmozfullscreenerror` | [`Document.onfullscreenerror`](https://developer.mozilla.org/docs/Web/API/Document/onfullscreenerror) |
| `Element.onmozfullscreenchange` | `Element.onfullscreenchange` |
| `Element.onmozfullscreenerror` | `Element.onfullscreenerror` |

**Events**: These events are now fired on the element first rather than `document`.

| Prefixed | Standard |
| --- | --- |
| `mozfullscreenchange` | [`fullscreenchange`](https://developer.mozilla.org/docs/Web/Events/fullscreenchange) |
| `mozfullscreenerror` | [`fullscreenerror`](https://developer.mozilla.org/docs/Web/Events/fullscreenerror) |

**CSS pseudo-class**:

| Prefixed | Standard |
| --- | --- |
| `:-moz-full-screen` | [`:fullscreen`](https://developer.mozilla.org/docs/Web/CSS/:fullscreen) |
