---
title: "非リリースビルドで Fullscreen API の接頭辞が外れました"
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
    - "/ja/docs/2016/fullscreen-api-has-been-unprefixed/"
---
Firefox 47 で [Fullscreen API](https://developer.mozilla.org/ja/docs/Web/API/Fullscreen_API) の接頭辞が外れました。非標準、接頭辞付きのメソッドとプロパティは廃止予定とみなされ、将来的に削除される可能性があります。

`element.mozRequestFullScreen`、[`document.mozCancelFullScreen`](https://developer.mozilla.org/ja/docs/Web/API/Document/mozCancelFullScreen) メソッドはそれぞれ [`element.requestFullscreen`](https://developer.mozilla.org/ja/docs/Web/API/Element/requestFullScreen)、`document.exitFullscreen` となりました。

[`document.mozFullScreenEnabled`](https://developer.mozilla.org/ja/docs/Web/API/Document/mozFullScreenEnabled)、[`document.mozFullScreenElement`](https://developer.mozilla.org/ja/docs/Web/API/Document/mozFullScreenElement) プロパティはそれぞれ `document.fullscreenEnabled`、`document.fullscreenElement` となりました。

[`document.mozFullScreen`](https://developer.mozilla.org/ja/docs/Web/API/Document/mozFullScreen) とまったく同じ標準プロパティはありません。`document.fullscreenElement` で代用してください。

`mozfullscreenchange`、`mozfullscreenerror` イベントはそれぞれ [`fullscreenchange`](https://developer.mozilla.org/ja/docs/Web/Events/fullscreenchange)、[`fullscreenerror`](https://developer.mozilla.org/ja/docs/Web/Events/fullscreenerror) となりました。

**更新**: いくつかのサイト互換性問題により、接頭辞なしの API は Beta、Release 両チャンネルでは [無効化](https://bugzilla.mozilla.org/show_bug.cgi?id=1268749) され、今後 [再び有効化](https://bugzilla.mozilla.org/show_bug.cgi?id=1269276) されることになりました。それに伴いこのドキュメントのタイトルを更新しました。ウェブ開発者がサイトをテストできるよう、接頭辞なしの API は Nightly、Aurora (Developer Edition) 両チャンネルでは引き続き有効化されます。なお、移行を容易にするため、`document.mozFullScreen` の接頭辞なし版として `document.fullscreen` を実装する [提案](https://bugzilla.mozilla.org/show_bug.cgi?id=1269157) が出されています。
