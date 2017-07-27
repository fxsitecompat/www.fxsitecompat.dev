---
title: "`getDefaultComputedStyle()` が削除されました"
date: "2017-04-16T03:00:00-04:00"
categories: ["dom"]
tags: []
versions: ["55"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1355683"
      title: "Bug 1355683 - Consider removing getDefaultComputedStyle"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/dGDkR65Ffa4/discussion"
      title: "Intent to unship: Window.getDefaultComputedStyle"
---
ブラウザによる要素上の既定計算値を返す非標準の [`window.getDefaultComputedStyle`](https://developer.mozilla.org/ja/docs/Web/API/Window/getDefaultComputedStyle) メソッドが Firefox 55 で削除されました。これは、似たような [`getComputedStyle`](https://developer.mozilla.org/ja/docs/Web/API/Window/getComputedStyle) メソッドと異なり、CSSOM 仕様の一部として標準化されたり他のブラウザに実装されたりすることはありませんでした。

jQuery 内で使用されていることが判明していますが、機能判別とフォールバックが適切に行われているため削除は問題とならないはずです。他の使用事例は確認されていません。

**更新**: 不可視インラインフレーム内で `getComputedStyle` が `null` を返すという、古いバージョンの jQuery に影響する [互換性問題](https://bugzilla.mozilla.org/show_bug.cgi?id=548397) により、この変更は Firefox 55 からバックアウトされました。しかし、`getDefaultComputedStyle` メソッドはいずれにしても将来的に削除されます。
