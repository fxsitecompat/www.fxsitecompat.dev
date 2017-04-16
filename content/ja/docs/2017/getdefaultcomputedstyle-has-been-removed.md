---
title: "`getDefaultComputedStyle()` が削除されました"
date: "2017-04-16T03:00:00-04:00"
categories: ["dom"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1355683"
      title: "Bug 1355683 - Consider removing getDefaultComputedStyle"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/dGDkR65Ffa4/discussion"
      title: "Intent to unship: Window.getDefaultComputedStyle"
---
ブラウザによる要素上の既定計算値を返す非標準の [`window.getDefaultComputedStyle`](https://developer.mozilla.org/ja/docs/Web/API/Window/getDefaultComputedStyle) メソッドが Firefox 55 で削除されました。これは、似たような [`getComputedStyle`](https://developer.mozilla.org/ja/docs/Web/API/Window/getComputedStyle) メソッドと異なり、CSSOM 仕様の一部として標準化されたり他のブラウザに実装されたりすることはありませんでした。

jQuery 内で使用されていることが判明していますが、機能判別とフォールバックが適切に行われているため削除は問題とならないはずです。他の使用事例は確認されていません。
