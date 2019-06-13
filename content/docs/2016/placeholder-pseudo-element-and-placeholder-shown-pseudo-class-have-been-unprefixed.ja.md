---
title: "`::placeholder` 擬似要素と `:placeholder-shown` 擬似クラスの接頭辞が外れました"
date: "2016-09-07T18:29:00-04:00"
categories: ["css"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1069012"
      title: "Bug 1069012 - unprefix :placeholder-shown pseudo-class and ::placeholder pseudo-element"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1069015"
      title: "Bug 1069015 - restore code for :placeholder-shown pseudo-class"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1300896"
      title: "Bug 1300896 - Remove prefixed ::-moz-placeholder pseudo-element and pseudo-class."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/ZdfheO1AXP0/discussion"
      title: "Intent to ship: CSS placeholder pseudo-element"
---
[`::placeholder`](https://developer.mozilla.org/docs/Web/CSS/::placeholder) CSS 擬似クラスの接頭辞が外されたため、[`::-moz-placeholder`](https://developer.mozilla.org/docs/Web/CSS/::-moz-placeholder) が廃止予定となりました。また、[Firefox 19 以降廃止予定となっている](https://www.fxsitecompat.dev/ja/docs/2012/moz-placeholder-pseudo-class-has-been-replaced-with-the-pseudo-element/)  [`:-moz-placeholder`](https://developer.mozilla.org/docs/Web/CSS/:-moz-placeholder) 擬似クラスの標準版として `:placeholder-shown` が追加されました。それぞれの接頭辞対応は将来的に廃止されます。
