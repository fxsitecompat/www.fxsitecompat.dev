---
title: "`border-image` が特定の状況で正しく表示されません"
date: "2016-12-01T01:58:00-05:00"
categories: ["css"]
tags: []
versions: ["50"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1315353"
      title: "Bug 1315353 - \"border-image: url(\"data:image/svg+xml\") repeat\" broken after implementation of space value of border-image-repeat"
---
[`border-image-repeat`](https://developer.mozilla.org/ja/docs/Web/CSS/border-image-repeat) CSS プロパティに追加された `space` 値の誤実装により、[`border-image`](https://developer.mozilla.org/ja/docs/Web/CSS/border-image) プロパティが部分的に反映されない場合があるというリグレッションが Firefox 50 で発生しました。このバグは Firefox 50.1.0 で修正されます。
