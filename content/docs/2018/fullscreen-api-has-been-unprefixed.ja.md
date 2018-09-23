---
title: "Fullscreen API の接頭辞が外れました"
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
何年にもわたるクロスブラウザー互換性向上の取り組みを経て、接頭辞なしの [Fullscreen API](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) が Firefox 64 ですべてのチャンネルにおいてようやく初期設定有効となりました。前回の接頭辞を外す試みは [Firefox 47](https://www.fxsitecompat.com/ja/docs/2016/fullscreen-api-has-been-unprefixed-in-non-release-builds/) で行われましたが、Nightly チャンネルを除いてすぐに取り消されていました。今後 `moz` 接頭辞付き API は廃止予定とみなされ、将来的に削除されます。

[Google Chrome 71](https://groups.google.com/a/chromium.org/d/topic/blink-dev/ODzbWn-xRrQ/discussion) も、Firefox 64 のリリースとほぼ同時期の 2018 年 12 月に、接頭辞なし API を提供する予定です。

**メソッド**: これらのメソッドは `Promise` を返すようになりました。

| 接頭辞付き | 標準 |
| --- | --- |
| `Document.mozCancelFullScreen()` | [`Document.exitFullscreen()`](https://developer.mozilla.org/docs/Web/API/Document/exitFullscreen) |
| `Element.mozRequestFullScreen()` | [`Element.requestFullscreen()`](https://developer.mozilla.org/docs/Web/API/Element/requestFullScreen) |

**プロパティ**:

| 接頭辞付き | 標準 |
| --- | --- |
| `Document.mozFullScreen` | [`Document.fullscreen`](https://developer.mozilla.org/docs/Web/API/Document/fullscreen) |
| `Document.mozFullScreenElement` | [`Document.fullscreenElement`](https://developer.mozilla.org/docs/Web/API/DocumentOrShadowRoot/fullscreenElement) |
| `Document.mozFullScreenEnabled` | [`Document.fullscreenEnabled`](https://developer.mozilla.org/docs/Web/API/Document/fullscreenEnabled) |
| `Document.onmozfullscreenchange` | [`Document.onfullscreenchange`](https://developer.mozilla.org/docs/Web/API/Document/onfullscreenchange) |
| `Document.onmozfullscreenerror` | [`Document.onfullscreenerror`](https://developer.mozilla.org/docs/Web/API/Document/onfullscreenerror) |
| `Element.onmozfullscreenchange` | `Element.onfullscreenchange` |
| `Element.onmozfullscreenerror` | `Element.onfullscreenerror` |

**イベント**: これらのイベントは `document` ではなく要素上で最初に発生するようになりました。

| 接頭辞付き | 標準 |
| --- | --- |
| `mozfullscreenchange` | [`fullscreenchange`](https://developer.mozilla.org/docs/Web/Events/fullscreenchange) |
| `mozfullscreenerror` | [`fullscreenerror`](https://developer.mozilla.org/docs/Web/Events/fullscreenerror) |

**CSS 擬似クラス**:

| 接頭辞付き | 標準 |
| --- | --- |
| `:-moz-full-screen` | [`:fullscreen`](https://developer.mozilla.org/docs/Web/CSS/:fullscreen) |
