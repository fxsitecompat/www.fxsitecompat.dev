---
title: "固定背景画像を持つ角丸オブジェクトが正しくトリミングされません"
date: "2015-12-18T17:37:00-05:00"
categories: ["css"]
tags: []
versions: ["43", "44"]
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1232939": "Bug 1232939 - The background image in a div is causing a spill over of the border where the border-radius cuts into the div"
---
`background-attachment` が `fixed` の場合に、`background-image` と `border-radius` CSS プロパティの組み合わせが期待通りに描画されず、オブジェクトの周りに単色の直角が表示されてしまうというリグレッションが Firefox 43 で発生しました。Mozilla の開発者が解決策に取り組んでいます。

**更新**: このバグは Firefox 45 で修正されました。
