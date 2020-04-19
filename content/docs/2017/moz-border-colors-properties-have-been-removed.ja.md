---
title: "`-moz-border-*-colors` プロパティが削除されました"
date: "2017-12-06T11:20:00-05:00"
categories: ["css"]
tags: []
versions: ["59", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1417200"
      title: "Bug 1417200 - Make -moz-border-*-colors chrome only"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/D23VvCJO53Q/discussion"
      title: "Intent to unship -moz-border-*-colors from content pages."
---
Firefox 59 以降、以下の非標準ボーダー色プロパティはウェブコンテンツから使用できなくなりました。

* [`-moz-border-top-colors`](https://developer.mozilla.org/docs/Web/CSS/-moz-border-top-colors)
* [`-moz-border-right-colors`](https://developer.mozilla.org/docs/Web/CSS/-moz-border-right-colors)
* [`-moz-border-bottom-colors`](https://developer.mozilla.org/docs/Web/CSS/-moz-border-bottom-colors)
* [`-moz-border-left-colors`](https://developer.mozilla.org/docs/Web/CSS/-moz-border-left-colors)

他のどのブラウザーもこれらに対応していないことから、互換性リスクは非常に低いはずです。まったく同じ標準プロパティはありませんが、必要であれば [`border-image`](https://developer.mozilla.org/docs/Web/CSS/border-image) を使ってグラデーション付きのボーダーを実現できます。
