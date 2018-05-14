---
title: "CSS3 Text Decoration プロパティの接頭辞が外れ、`text-decoration` はショートハンドになりました"
date: "2014-12-19T11:15:21-05:00"
categories: ["css"]
tags: []
versions: ["36"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=825004"
      title: "Bug 825004 – [css-text-decor-3] Unprefix CSS3 Text Decoration"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1039488"
      title: "Bug 1039488 – support the full css3-text-decor syntax for the \'text-decoration\' shorthand rather than only the CSS2.1 syntax"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1097922"
      title: "Bug 1097922 – Remove temporary aliases for -moz-text-decoration-*."
---
[`text-decoration`](https://developer.mozilla.org/docs/Web/CSS/text-decoration) プロパティが [CSS3 Text Decoration Module Level 3](https://drafts.csswg.org/css-text-decor-3/) に準拠し、この仕様で定義された [`text-decoration-line`](https://developer.mozilla.org/docs/Web/CSS/text-decoration-line)、[`text-decoration-color`](https://developer.mozilla.org/docs/Web/CSS/text-decoration-color)、[`text-decoration-style`](https://developer.mozilla.org/docs/Web/CSS/text-decoration-style) 各プロパティの接頭辞が外れました。`text-decoration` は [ショートハンドプロパティ](https://developer.mozilla.org/docs/Web/CSS/Shorthand_properties) になりましたが、CSS 2.1 準拠だったこれまで通り、`text-decoration-color` と `text-decoration-style` がいずれも [初期値](https://developer.mozilla.org/docs/Web/CSS/initial_value) であるかのように動作します。接頭辞付き `-moz-text-decoration-*` プロパティへの対応はまだ残されていますが、今後数バージョン以内に削除されます。

**更新**: これらの接頭辞付きプロパティは [Firefox 40 で削除されました](https://www.fxsitecompat.com/ja/docs/2015/moz-text-decoration-properties-have-been-removed/)。
