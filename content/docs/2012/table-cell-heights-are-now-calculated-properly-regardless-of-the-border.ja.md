---
title: "ボーダーによってテーブルセルの高さが変わる問題が修正されました"
date: "2012-10-09T06:00:00-04:00"
categories: ["css"]
tags: []
versions: ["16"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=248239"
      title: "Bug 248239 – borders and padding on the top and bottom of table cells reduce the height"
---
これまで、テーブルセルすなわち [`<td>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/td) 要素の上下に `border` や `padding` が指定されると、その分セルの高さが縮まって表示されていました。Firefox 16 では、CSS 仕様に従うよう、このレイアウト問題が修正されています。実際の例はバグに添付されたテストケースを参照してください。
