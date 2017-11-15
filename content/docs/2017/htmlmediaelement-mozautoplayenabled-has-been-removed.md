---
title: "`HTMLMediaElement.mozAutoplayEnabled` has been removed"
date: "2017-11-15T10:46:00-05:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1336400"
      title: "Bug 1336400 - Remove HTMLMediaElement::mozAutoplayEnabled"
---
The non-standard `mozAutoplayEnabled` boolean property on the [`HTMLMediaElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement) interface, that returns if media autoplay is enabled in the browser, has been removed with Firefox 59 as it has never been standardized.

Web developers should basically avoid using the autoplay functionality because it leads to a poor user experience in many cases. Still, it's possible to start playing media programmatically instead of with the [`autoplay`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/autoplay) attribute on the element.
