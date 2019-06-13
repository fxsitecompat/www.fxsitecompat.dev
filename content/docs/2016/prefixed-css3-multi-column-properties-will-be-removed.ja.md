---
title: "接頭辞付き CSS3 マルチカラムプロパティが削除されます"
date: "2016-10-10T20:57:00-04:00"
categories: ["css"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=698783"
      title: "Bug 698783 - Remove prefixing for CSS3 multicol"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/EammrHjrCpw/discussion"
      title: "Intent to ship: css multi-column properties (unprefixed)"
---
[Firefox 52 以降廃止予定となっている](https://www.fxsitecompat.dev/ja/docs/2016/css3-multi-column-properties-have-been-unprefixed/) `-moz` 接頭辞付きマルチカラムプロパティへの対応は、近い将来削除される予定です。[`column-count`](https://developer.mozilla.org/docs/Web/CSS/column-count)、[`column-fill`](https://developer.mozilla.org/docs/Web/CSS/column-fill)、[`column-gap`](https://developer.mozilla.org/docs/Web/CSS/column-gap)、[`column-rule`](https://developer.mozilla.org/docs/Web/CSS/column-rule)、[`column-rule-color`](https://developer.mozilla.org/docs/Web/CSS/column-rule-color)、[`column-rule-style`](https://developer.mozilla.org/docs/Web/CSS/column-rule-style)、[`column-rule-width`](https://developer.mozilla.org/docs/Web/CSS/column-rule-width)、[`column-width`](https://developer.mozilla.org/docs/Web/CSS/column-width)、[`columns`](https://developer.mozilla.org/docs/Web/CSS/columns) といった標準プロパティを使うようにしてください。
