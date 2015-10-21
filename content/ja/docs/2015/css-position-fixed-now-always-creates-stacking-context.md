---
title: "CSS `position:fixed` が常にスタック文脈を生成するようになりました"
date: "2015-10-03T11:43:00-04:00"
categories: ["css"]
tags: []
versions: ["44"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1179288": "Bug 1179288 - change position:fixed so it always creates a stacking context"
---
CSS 仕様書が更新され、Web 互換性のため [`position:fixed`](https://developer.mozilla.org/ja/docs/Web/CSS/position#Fixed_positioning) が常に [スタック文脈](https://developer.mozilla.org/ja/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context) を生成するよう変更が加えられました。新しい挙動は Chrome と Safari に一致するはずですが、以前の Firefox のレンダリングに依存しているページやアプリはこの変更によって影響を受ける可能性があります。
