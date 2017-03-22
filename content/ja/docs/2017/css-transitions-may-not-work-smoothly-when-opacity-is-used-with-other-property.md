---
title: "`opacity` が他のプロパティととともに使われた場合、CSS トランジションがスムーズに動かない場合があります"
date: "2017-03-21T19:50:00-04:00"
categories: ["css"]
tags: []
versions: ["52"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1318697"
      title: "Bug 1318697 - Elements disappear after sliding in"
---
`opacity` プロパティが `transform` や `visibility` といった他の特定のプロパティと同時に変更された場合、[CSS トランジション](https://developer.mozilla.org/ja/docs/Web/CSS/CSS_Transitions) が指定通りに適用されないというリグレッションが Firefox 52 で発生しました。影響を受ける要素はトランジション実行中に点滅したり、直後に消えたりする可能性があります。このバグは Firefox 53 Beta で修正されました。
