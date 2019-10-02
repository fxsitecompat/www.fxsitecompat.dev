---
title: "CSS 円形グラデーションが負の半径を受け付けなくなりました"
date: "2019-10-02T17:07:00-04:00"
categories: ["css"]
tags: []
versions: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1583736"
      title: "Bug 1583736 - CSS radial-gradient should not accept negative radii"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vCIpV5oCAtg/discussion"
      title: "Intent to unship: Negative radii in radial gradients."
---
Firefox 71 以降、接頭辞付き、接頭辞なし双方の [`radial-gradient()`](https://developer.mozilla.org/docs/Web/CSS/radial-gradient) CSS 関数が、何らかの負の長さを含んだ引数を無視するようになります。これは仕様では無効とされていましたが、すべてのブラウザーが対応していました。例えば以下の宣言は今後機能しなくなります。

```css
background-image: radial-gradient(-100px 25px, red, green);
background-image: -moz-radial-gradient(50%, -100px -10%, red, blue);
background-image: -webkit-gradient(radial, 1 2, -1.5, 50% 50%, 10000);
```

[Google Chrome](https://bugs.chromium.org/p/chromium/issues/detail?id=1008112) は最近のバージョンで同様の変更を行い、[Safari](https://bugs.webkit.org/show_bug.cgi?id=202412) も追従する見通しです。
