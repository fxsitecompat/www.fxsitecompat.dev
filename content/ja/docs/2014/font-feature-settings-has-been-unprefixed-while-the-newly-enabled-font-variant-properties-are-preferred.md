---
title: "`font-feature-settings` の接頭辞が外れましたが、新たに有効化された `font-variant-*` プロパティが推奨されています"
date: "2014-09-01T22:12:15-04:00"
categories: ["css"]
tags: []
versions: "34"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=835191": "Bug 835191 – Unprefix -moz-font-feature-settings"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=975744": "Bug 975744 – enable font-variant-* / font-feature in release by default"
---
CSS3 Fonts Module 仕様で定義された次のプロパティが初期設定で有効化されました。[`font-kerning`](https://developer.mozilla.org/ja/docs/Web/CSS/font-kerning)、[`font-synthesis`](https://developer.mozilla.org/ja/docs/Web/CSS/font-synthesis)、[`font-variant`](https://developer.mozilla.org/ja/docs/Web/CSS/font-variant)、[`font-variant-alternates`](https://developer.mozilla.org/ja/docs/Web/CSS/font-variant-alternates)、[`font-variant-caps`](https://developer.mozilla.org/ja/docs/Web/CSS/font-variant-caps)、[`font-variant-east-asian`](https://developer.mozilla.org/ja/docs/Web/CSS/font-variant-east-asian)、[`font-variant-ligatures`](https://developer.mozilla.org/ja/docs/Web/CSS/font-variant-ligatures)、[`font-variant-numeric`](https://developer.mozilla.org/ja/docs/Web/CSS/font-variant-numeric)、[`font-variant-position`](https://developer.mozilla.org/ja/docs/Web/CSS/font-variant-position)

これと同時に、[`font-feature-settings`](https://developer.mozilla.org/ja/docs/Web/CSS/font-feature-settings)、[`font-language-override`](https://developer.mozilla.org/ja/docs/Web/CSS/font-language-override) 両プロパティの接頭辞も外れ、接頭辞付きの各プロパティは今後削除されます。Web 制作者には今後、低レベル `font-feature-settings` プロパティの代わりに、分かりやすい新たな `font-variant-*` プロパティの使用を推奨します。
