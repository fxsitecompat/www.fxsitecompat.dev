---
title: "`min-width` と `min-height` の初期値が `auto` に変わりました"
date: "2012-12-03T03:53:26-05:00"
categories: ["css"]
tags: []
versions: ["18", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=763689"
      title: "Bug 763689 – New initial value for \"min-width\" & \"min-height\": auto"
---
[`min-width`](https://developer.mozilla.org/docs/CSS/min-width)、[`min-height`](https://developer.mozilla.org/docs/CSS/min-height) 両プロパティが [初期値](https://developer.mozilla.org/docs/CSS/initial_value) として [`auto`](https://developer.mozilla.org/docs/CSS/auto) キーワードを取るようになりました。Firefox 18 で実装され初期設定では無効となっている [フレキシブルボックス (flexbox)](https://developer.mozilla.org/docs/CSS/Using_CSS_flexible_boxes) では、この `auto` キーワードは flexbox 内の最小アイテム (`min-content`) を示します。それ以外の要素では、従来通り `0` と計算されるため影響はありません。
