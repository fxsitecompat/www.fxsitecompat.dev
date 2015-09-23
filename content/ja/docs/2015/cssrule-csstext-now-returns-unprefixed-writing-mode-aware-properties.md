---
title: "`CSSRule.cssText` が接頭辞なしの `writing-mode` 関連プロパティを返すようになりました"
date: "2015-09-22T11:24:00-04:00"
categories: ["css"]
tags: []
versions: "42"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1118103": "Bug 1118103 - swap the aliasing direction of -moz-margin-start <-> margin-inline-start etc."
---
[Firefox 41](https://developer.mozilla.org/ja/Firefox/Releases/41#CSS) で東アジア言語向けの縦書き対応が初期設定有効となり、[`writing-mode`](https://developer.mozilla.org/ja/docs/Web/CSS/writing-mode) CSS プロパティと、方向に依存しない様々な `margin`、`border`、`padding` 関連のプロパティが追加されました。

Firefox 41 リリースの時点で、[`CSSRule.cssText`](https://developer.mozilla.org/ja/docs/Web/API/CSSRule/cssText) によって返されるプロパティ名などシリアライズされたスタイルルールや、スタイルルール内のプロパティ反復は、[`margin-inline-start`](https://developer.mozilla.org/ja/docs/Web/CSS/margin-inline-start) など接頭辞なしの正規形式ではなく、`-moz-margin-start` など接頭辞付きの旧形式となっていました。この問題は Firefox 42 で接頭辞付きと接頭辞なしプロパティの内部エイリアス方向を逆転させることで修正されました。

それらの接頭辞付きプロパティは廃止予定となっており、将来的に対応は打ち切られます。
