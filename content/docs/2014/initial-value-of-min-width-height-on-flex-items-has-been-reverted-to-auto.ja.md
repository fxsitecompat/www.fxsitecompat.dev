---
title: "可変アイテム上の `min-width`/`height` の初期値が `auto` へ戻されました"
date: "2014-09-01T22:12:15-04:00"
categories: ["css"]
tags: []
versions: ["34"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=984711"
      title: "Bug 984711 – Add back \"min-width:auto\" / \"min-height:auto\" for flex items"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1015474"
      title: "Bug 1015474 – Update min-width:auto/min-height:auto support to match updated flexbox spec language"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1057683"
      title: "Bug 1057683 – http://i100.independent.co.uk/ is broken in Nightly, due to the new \"min-height:auto\" flex item behavior (from flexbox spec change)"
---
[Firefox 22](https://www.fxsitecompat.com/ja/docs/2013/initial-value-for-min-width-and-min-height-has-been-changed-back-to-0-even-on-flex-items/) 以降、[`min-width`](https://developer.mozilla.org/docs/Web/CSS/min-width)、[`min-height`](https://developer.mozilla.org/docs/Web/CSS/min-height) 両プロパティの [初期値](https://developer.mozilla.org/docs/Web/CSS/initial_value) は [可変アイテム](https://developer.mozilla.org/docs/Web/Guide/CSS/Flexible_boxes) 上であっても `0` となっていました。最新の CSS Flexible Box Layout Module 仕様に従い、この値は可変ボックス内の最小アイテム (`min-content`) サイズに相当する [`auto`](https://developer.mozilla.org/docs/Web/CSS/auto) に戻されました。可変アイテム以外では変わらず `0` となっています。あなたが管理しているスタイルシートに可変アイテムが含まれる場合は、[Firefox Aurora](https://www.mozilla.org/firefox/channel/#aurora) でページをテストし、従来通りの挙動を保つには明示的に `min-height:0` を定義すると良いでしょう。
