---
title: "CSS3 マルチカラムプロパティの接頭辞が外れました"
date: "2016-10-10T20:34:00-04:00"
categories: ["css"]
tags: []
versions: ["52"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1300895"
      title: "Bug 1300895 - Unprefix css3 multi-column properties (and add back -moz prefixed versions as aliases, for now)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=616436"
      title: "Bug 616436 - column-span not implemented (css3 multicolumn)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/EammrHjrCpw/discussion"
      title: "Intent to ship: css multi-column properties (unprefixed)"
---
[`column-count`](https://developer.mozilla.org/docs/Web/CSS/column-count)、[`column-fill`](https://developer.mozilla.org/docs/Web/CSS/column-fill)、[`column-gap`](https://developer.mozilla.org/docs/Web/CSS/column-gap)、[`column-rule`](https://developer.mozilla.org/docs/Web/CSS/column-rule)、[`column-rule-color`](https://developer.mozilla.org/docs/Web/CSS/column-rule-color)、[`column-rule-style`](https://developer.mozilla.org/docs/Web/CSS/column-rule-style)、[`column-rule-width`](https://developer.mozilla.org/docs/Web/CSS/column-rule-width)、[`column-width`](https://developer.mozilla.org/docs/Web/CSS/column-width)、[`columns`](https://developer.mozilla.org/docs/Web/CSS/columns) 各プロパティの接頭辞が Firefox 52 で外れました。`-moz` 接頭辞付きのプロパティはエイリアスとして残りますが、[近い将来削除されます](https://www.fxsitecompat.dev/ja/docs/2016/prefixed-css3-multi-column-properties-will-be-removed/)。

なお、Firefox はまだ [`column-span`](https://developer.mozilla.org/docs/Web/CSS/column-span) プロパティには対応していません。
