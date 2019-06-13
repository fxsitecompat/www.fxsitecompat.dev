---
title: "接頭辞付き `-moz-initial` への対応が打ち切られました"
date: "2013-05-19T07:35:00-04:00"
categories: ["css"]
tags: []
versions: ["24"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=807184"
      title: "Bug 807184 – Remove support for prefixed \"-moz-initial\" CSS keyword, now that we support it unprefixed"
---
接頭辞付き `-moz-initial` キーワードへの対応が Firefox 24 で削除されました。[Firefox 19](https://www.fxsitecompat.dev/ja/docs/2012/moz-initial-has-been-unprefixed/) 以降、接頭辞なしの [`initial`](https://developer.mozilla.org/docs/Web/CSS/initial) キーワードで代用可能となっています。
