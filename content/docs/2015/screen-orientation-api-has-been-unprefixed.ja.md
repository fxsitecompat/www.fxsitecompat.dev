---
title: "Screen Orientation API の接頭辞が外れました"
date: "2015-09-09T17:20:00-04:00"
categories: ["dom"]
tags: []
versions: ["43"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1131470"
      title: "Bug 1131470 - w3c screen orientation api has changed"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/zyGP6PemJlg/discussion"
      title: "Intent to Ship: Screen Orientation API"
---
Firefox 43 で最新の標準 [Screen Orientation API](https://w3c.github.io/screen-orientation/) が実装されました。これは `window.screen.orientation` 上で `type`、`angle`、`onchange` の各プロパティと `lock`、`unlock` 両メソッドを提供します。

Firefox 14 以降利用可能な実験的接頭辞付き実装には、[`window.screen`](https://developer.mozilla.org/docs/Web/API/Screen) 上の `mozOrientation`、`onmozorientationchange` 両プロパティと `mozLockOrientation`、`mozUnlockOrientation` 両メソッドが含まれますが、これらは将来的に削除されます。
