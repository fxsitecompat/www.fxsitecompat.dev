---
title: "`displaystyle` がルートの `<math>` 要素から継承されなくなりました"
date: "2014-02-07T11:57:09-05:00"
categories: ["misc"]
tags: []
versions: ["29", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=838506"
      title: "Bug 838506 – Refactor implementation of displaystyle using a -moz-display-style property"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1011237"
      title: "Bug 1011237 – Explicit displaystyle=\"true\" on root <math> element is not inherited"
---
`displaystyle` 属性の実装が、仕様へ準拠するためにリファクタリングされました。[`<mtable>`](https://developer.mozilla.org/docs/Web/MathML/Element/mtable) 要素上の `displaystyle` はルートの [`<math>`](https://developer.mozilla.org/docs/Web/MathML/Element/math) 要素から継承されなくなりました。この属性が存在しない場合、`displaystyle` の既定値である `false` と見なされます。この仕組みについては [デフォルトスタイルシード](https://dxr.mozilla.org/mozilla-release/source/layout/mathml/mathml.css) を参照してください。
