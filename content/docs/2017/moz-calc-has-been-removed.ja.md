---
title: "`-moz-calc()` が廃止されました"
date: "2017-01-18T10:27:00-05:00"
categories: ["css"]
tags: []
versions: ["53"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1331296"
      title: "Bug 1331296 - Remove support for -moz-calc()"
---
接頭辞付き `-moz-calc` CSS 関数への対応が Firefox 53 で廃止されました。[Firefox 16](https://www.fxsitecompat.dev/ja/docs/2012/various-css-properties-have-been-unprefixed/) 以降対応している標準の接頭辞なし [`calc`](https://developer.mozilla.org/docs/Web/CSS/calc) 関数を使用してください。
