---
title: "方向非依存 CSS プロパティの接頭辞が外れました"
date: "2015-09-24T14:26:00-04:00"
categories: ["css"]
tags: []
versions: ["41"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1138384"
      title: "Bug 1138384 - enable CSS writing-mode support in release channels"
---
CSS3 Writing Modes 実装の一環として、アラビア語など <abbr title="Right-to-Left">RTL</abbr> 言語への対応を容易にするために使用可能な、`margin`、`border`、`padding` のための方向に依存しない各種 CSS プロパティから接頭辞が外れました。以下の表が示す通り、接頭辞なしプロパティは単に `-moz-` を外したものではないため、これらを使う場合には注意が必要です。

| 接頭辞付きプロパティ        | 接頭辞なしプロパティ                                                                                     |
| ------------------------- | ------------------------------------------------------------------------------------------------------ |
| `-moz-margin-start`       | [`margin-inline-start`](https://developer.mozilla.org/ja/docs/Web/CSS/margin-inline-start)             |
| `-moz-margin-end`         | [`margin-inline-end`](https://developer.mozilla.org/ja/docs/Web/CSS/margin-inline-end)                 |
| `-moz-border-start`       | [`border-inline-start`](https://developer.mozilla.org/ja/docs/Web/CSS/border-inline-start)             |
| `-moz-border-start-width` | [`border-inline-start-width`](https://developer.mozilla.org/ja/docs/Web/CSS/border-inline-start-width) |
| `-moz-border-start-style` | [`border-inline-start-style`](https://developer.mozilla.org/ja/docs/Web/CSS/border-inline-start-style) |
| `-moz-border-start-color` | [`border-inline-start-color`](https://developer.mozilla.org/ja/docs/Web/CSS/border-inline-start-color) |
| `-moz-border-end`         | [`border-inline-end`](https://developer.mozilla.org/ja/docs/Web/CSS/border-inline-end)                 |
| `-moz-border-end-width`   | [`border-inline-end-width`](https://developer.mozilla.org/ja/docs/Web/CSS/border-inline-end-width)     |
| `-moz-border-end-style`   | [`border-inline-end-style`](https://developer.mozilla.org/ja/docs/Web/CSS/border-inline-end-style)     |
| `-moz-border-end-color`   | [`border-inline-end-color`](https://developer.mozilla.org/ja/docs/Web/CSS/border-inline-end-color)     |
| `-moz-padding-start`      | [`padding-inline-start`](https://developer.mozilla.org/ja/docs/Web/CSS/padding-inline-start)           |
| `-moz-padding-end`        | [`padding-inline-end`](https://developer.mozilla.org/ja/docs/Web/CSS/padding-inline-start)             |

バグにより、Firefox 41 は、ページインスペクタ、[`CSSRule.cssText`](https://developer.mozilla.org/ja/docs/Web/API/CSSRule/cssText)、その他 API においてまだ接頭辞付きプロパティを表示しています。この問題は [Firefox 42 で修正されました](https://www.fxsitecompat.com/ja/docs/2015/cssrule-csstext-now-returns-unprefixed-writing-mode-aware-properties/)。

接頭辞付きプロパティへの対応は将来的に打ち切られます。
