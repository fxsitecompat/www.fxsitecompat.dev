---
title: "Fullscreen API の接頭辞が外れました"
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
Firefox 47 で [Fullscreen API](https://developer.mozilla.org/ja/docs/Web/API/Fullscreen_API) の接頭辞が外れました。非標準、接頭辞付きのメソッドとプロパティは廃止予定とみなされ、将来的に削除される可能性があります。

`element.mozRequestFullScreen`、[`document.mozCancelFullScreen`](https://developer.mozilla.org/ja/docs/Web/API/Document/mozCancelFullScreen) メソッドはそれぞれ [`element.requestFullscreen`](https://developer.mozilla.org/ja/docs/Web/API/Element/requestFullScreen)、`document.exitFullscreen` となりました。

[`document.mozFullScreenEnabled`](https://developer.mozilla.org/ja/docs/Web/API/Document/mozFullScreenEnabled)、[`document.mozFullScreenElement`](https://developer.mozilla.org/ja/docs/Web/API/Document/mozFullScreenElement) プロパティはそれぞれ `document.fullscreenEnabled`、`document.fullscreenElement` となりました。

[`document.mozFullScreen`](https://developer.mozilla.org/ja/docs/Web/API/Document/mozFullScreen) とまったく同じ標準プロパティはありません。`document.fullscreenElement` で代用してください。

`mozfullscreenchange`、`mozfullscreenerror` イベントはそれぞれ [`fullscreenchange`](https://developer.mozilla.org/ja/docs/Web/Events/fullscreenchange)、[`fullscreenerror`](https://developer.mozilla.org/ja/docs/Web/Events/fullscreenerror) となりました。
