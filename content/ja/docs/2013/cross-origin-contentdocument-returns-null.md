---
title: "クロスオリジン `contentDocument` が `null` を返します"
date: "2013-04-06T04:52:59-04:00"
categories: ["dom"]
tags: []
versions: "23"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=829872": "Bug 829872 – Consider returning null from contentDocument getters when the caller does not subsume the document"
---
フレーム上の `contentDocument` プロパティが、スクリプトの呼び出し元にそのドキュメントが含まれない場合、[`null`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/null) を返すようになりました。この変更は、[`<frame>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/frame)、[`<iframe>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/iframe)、[`<object>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/object) 要素上の `contentDocument` プロパティ、および [`<embed>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/embed)、[`<iframe>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/iframe)、[`<object>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/object) 要素上の [`getSVGDocument`](https://developer.mozilla.org/ja/docs/Web/SVG/Scripting#_.E6.96.87.E6.9B.B8.E9.96.93.E3.81.AE.E3.82.B9.E3.82.AF.E3.83.AA.E3.83.97.E3.83.86.E3.82.A3.E3.83.B3.E3.82.B0_-_.E5.9F.8B.E3.82.81.E8.BE.BC.E3.81.BF_SVG_.E3.81.AE.E5.8F.82.E7.85.A7_) メソッドに影響します。
