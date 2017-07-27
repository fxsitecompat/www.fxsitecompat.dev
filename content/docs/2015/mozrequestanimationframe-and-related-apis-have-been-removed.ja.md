---
title: "`mozRequestAnimationFrame` と関連する API が削除されました"
date: "2015-08-05T00:48:18-04:00"
categories: ["dom"]
tags: []
versions: ["42"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=909154"
      title: "Bug 909154 - Consider removing support for the prefixed mozRequestAnimationFrame"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/nULjUn_Zg1w/discussion"
      title: "Intent to unship: Prefixed mozRequestAnimationFrame and related APIs (mozAnimationStartTime, mozCancelAnimationFrame)"
---
[Firefox 23 以降廃止予定となっていた](https://www.fxsitecompat.com/ja/docs/2013/requestanimationframe-and-cancelanimationframe-have-been-unprefixed/) `mozRequestAnimationFrame`、`mozCancelAnimationFrame`、`mozCancelRequestAnimationFrame` の各メソッドが、標準の [`requestAnimationFrame`](https://developer.mozilla.org/ja/docs/Web/API/Window/requestAnimationFrame)、[`cancelAnimationFrame`](https://developer.mozilla.org/ja/docs/Web/API/Window/cancelAnimationFrame) メソッドに置き換えられる形で削除されました。[`mozAnimationStartTime`](https://developer.mozilla.org/ja/docs/Web/API/Window/mozAnimationStartTime) プロパティも削除されましたが、他のブラウザーは同等のプロパティを実装していないため、互換性への影響は軽微なはずです。
