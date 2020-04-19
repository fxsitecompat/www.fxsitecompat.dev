---
title: "`-moz-element()` で指定された背景画像が更新されません"
date: "2012-12-03T03:54:45-05:00"
categories: ["css"]
tags: []
versions: ["19", "24-esr"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=909157"
      title: "Bug 909157 – -moz-element background fails to update after image reloads"
---
[`-moz-element`](https://developer.mozilla.org/docs/Web/CSS/-moz-element) 関数で指定された CSS 背景画像が、元要素の [`background-image`](https://developer.mozilla.org/docs/Web/CSS/background-image) が動的に変更された際に更新されません。これは Firefox 19 以来のりグレションで、Firefox 26 で修正されました。
