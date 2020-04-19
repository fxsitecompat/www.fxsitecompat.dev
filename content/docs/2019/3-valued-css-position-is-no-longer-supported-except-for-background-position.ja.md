---
title: "3 値の CSS 位置指定は `background-position` を除き使用できなくなりました"
date: "2019-07-11T23:27:00-04:00"
categories: ["css"]
tags: []
releases: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1559276"
      title: "Bug 1559276 - Retiring support for 3-valued <position> (excluding background)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/zZ9FMk4OAsc/discussion"
      title: "Intent to unship: 3-valued position syntax from <object-position>, <perspective-origin>, <mask-position>"
---
現行の [CSS Values 仕様](https://drafts.csswg.org/css-values-4/#position) に従い、`object-position`、`perspective-origin`、`mask-position` プロパティおよび `circle`、`ellipse` シェイプ関数向けの 3 値ポジション構文への対応が Firefox 70 で廃止されました。今後は 1、2、4 値の構文のみ使用可能となります。ただし、`background-position` は今後も `left 10px top` のような 3 値構文を受け入れます。

[Google Chrome](https://www.chromestatus.com/feature/5116559680864256) は既に同じ変更をバージョン 68 で行っています。
