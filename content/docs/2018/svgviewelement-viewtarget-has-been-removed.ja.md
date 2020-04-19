---
title: "`SVGViewElement.viewTarget` が削除されました"
date: "2018-04-25T18:18:00-04:00"
categories: ["dom", "svg"]
tags: []
versions: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1455763"
      title: "Bug 1455763 - Remove SVGViewElement.viewTarget"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/3rbtcFOcVjI/discussion"
      title: "Intent to unship: SVGViewElement.viewTarget"
aliases:
    - "/ja/docs/2018/svgviewelement-prototype-viewtarget-has-been-removed/"
---
[`SVGViewElement`](https://developer.mozilla.org/docs/Web/API/SVGViewElement) 上の `viewTarget` プロパティが Firefox 61 で削除されました。これは SVG 1.1 仕様で定義されていましたが、使用例がないことから SVG 2 では削除されています。また、Firefox では正しい実装が行われておらず、単にエラーが返されるだけでした。

2017 年 1 月公開の [Google Chrome 56](https://www.chromestatus.com/feature/5665473114931200) が既にこの変更を行っていることから、互換性リスクは低いはずです。
