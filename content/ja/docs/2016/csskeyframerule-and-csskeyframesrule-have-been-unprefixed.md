---
title: "`CSSKeyframeRule` と `CSSKeyframesRule` の接頭辞が外れました"
date: "2016-03-16T05:34:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["48"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1256178"
      title: "Bug 1256178 - Drop the moz prefix from the MozCSSKeyframeRule and MozCSSKeyframesRule interfaces"
---
接頭辞付きの `MozCSSKeyframeRule`、`MozCSSKeyframesRule` 両インタフェースが、それぞれ標準の [`CSSKeyframeRule`](https://developer.mozilla.org/ja/docs/Web/API/CSSKeyframeRule)、[`CSSKeyframesRule`](https://developer.mozilla.org/ja/docs/Web/API/CSSKeyframesRule) インタフェースに置き換えられました。Firefox 48 以降、接頭辞付きのものは使用不可となります。
