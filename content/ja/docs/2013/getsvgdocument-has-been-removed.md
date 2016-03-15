---
title: "`GetSVGDocument` が削除されました"
date: "2013-05-19T07:35:00-04:00"
categories: ["svg"]
tags: []
versions: ["24"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=881128"
      title: "Bug 881128 – Remove nsIDOMGetSVGDocument"
---
`GetSVGDocument` インタフェースが削除されました。他のどのブラウザもこれを [`window`](https://developer.mozilla.org/ja/docs/Web/API/window) オブジェクト上に露呈していません。[`<embed>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/embed)、[`<iframe>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/iframe)、[`<object>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/object) 要素上の [`getSVGDocument`](https://developer.mozilla.org/ja/docs/Web/SVG/Scripting#_.E6.96.87.E6.9B.B8.E9.96.93.E3.81.AE.E3.82.B9.E3.82.AF.E3.83.AA.E3.83.97.E3.83.86.E3.82.A3.E3.83.B3.E3.82.B0_-_.E5.9F.8B.E3.82.81.E8.BE.BC.E3.81.BF_SVG_.E3.81.AE.E5.8F.82.E7.85.A7_) メソッドは今後も使用可能です。
