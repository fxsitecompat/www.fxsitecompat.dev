---
title: "`CSSRule.cssText` が接頭辞なしの `writing-mode` 関連プロパティを返すようになりました"
date: "2015-09-22T11:24:00-04:00"
categories: ["css"]
tags: []
versions: ["42"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1118103"
      title: "Bug 1118103 - swap the aliasing direction of -moz-margin-start <-> margin-inline-start etc."
---
[Firefox 41](https://developer.mozilla.org/Firefox/Releases/41#CSS) で東アジア言語向けの縦書き対応が初期設定有効となり、[`writing-mode`](https://developer.mozilla.org/docs/Web/CSS/writing-mode) CSS プロパティと、方向に依存しない様々な `margin`、`border`、`padding` 関連のプロパティが追加されました。それと同時に、いくつかの既存のプロパティは [接頭辞が外れました](https://www.fxsitecompat.com/ja/docs/2015/direction-independent-css-properies-have-been-unprefixed/)。

Firefox 41 リリースの時点で、[`CSSRule.cssText`](https://developer.mozilla.org/docs/Web/API/CSSRule/cssText) によって返されるプロパティ名などシリアライズされたスタイルルールや、スタイルルール内のプロパティ反復は、[`margin-inline-start`](https://developer.mozilla.org/docs/Web/CSS/margin-inline-start) など接頭辞なしの正規形式ではなく、`-moz-margin-start` など接頭辞付きの旧形式となっていました。[ページインスペクターの CSS ペイン](https://developer.mozilla.org/docs/Tools/Page_Inspector/How_to/Examine_and_edit_CSS) も、接頭辞なしプロパティへの対応が既に追加されているにも関わらず、接頭辞付きプロパティを表示していました。この問題は Firefox 42 で接頭辞付きと接頭辞なしプロパティの内部エイリアス方向を逆転させることで修正されました。

それらの接頭辞付きプロパティは廃止予定となっており、将来的に対応は打ち切られます。
