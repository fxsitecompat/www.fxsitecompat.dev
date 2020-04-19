---
title: "`::-moz-math-stretchy` 疑似要素が削除されました"
date: "2014-04-03T19:31:02-04:00"
categories: ["css"]
tags: []
versions: ["31", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1000879"
      title: "Bug 1000879 – Remove the ::-moz-math-stretchy pseudo-element."
---
非標準の `::-moz-math-stretchy` 疑似要素への対応が削除されました。これはページ作者が伸縮可能演算子に使用する [`font-family`](https://developer.mozilla.org/docs/Web/CSS/font-family) を指定できるようにするものでした。現在は、[`<math>`](https://developer.mozilla.org/docs/Web/HTML/Element/math) 要素上で指定した [数式フォント](https://developer.mozilla.org/docs/Mozilla/MathML_Project/Fonts) が子ノードにも継承されるようになっています。
