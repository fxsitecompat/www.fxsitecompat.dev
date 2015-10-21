---
title: "`min-width` と `min-height` の初期値が (flexbox アイテム上でも) `0` に戻されました"
date: "2013-02-24T03:44:31-05:00"
categories: ["css"]
tags: []
versions: ["22"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=848539": "Bug 848539 – Remove support for \"min-width: auto\" and \"min-height: auto\", since they\'re being dropped from flexbox spec"
---
[Firefox 18](https://www.fxsitecompat.com/ja/docs/2012/initial-value-for-min-width-and-min-height-has-been-changed-to-auto/) 以降、[`min-width`](https://developer.mozilla.org/ja/docs/Web/CSS/min-width)、[`min-height`](https://developer.mozilla.org/ja/docs/Web/CSS/min-height) プロパティが [初期値](https://developer.mozilla.org/ja/docs/Web/CSS/initial_value) として [`auto`](https://developer.mozilla.org/ja/docs/Web/CSS/auto) キーワードを取るようになりました。これは多くの場合 `0` として計算されていましたが、[flex アイテム上では特別な挙動](http://www.w3.org/TR/2012/CR-css3-flexbox-20120918/#min-size-auto) をしていました。この値は CSS [フレキシブルボックス (flexbox)](https://developer.mozilla.org/ja/docs/Web/Guide/CSS/Flexible_boxes) 仕様の旧バージョンで導入されましたが、その後のバージョンの仕様では [値が削除されました](https://dvcs.w3.org/hg/csswg/rev/9437131b3d6e#l1.86)。そのため、これらのプロパティの初期値は、[CSS 2.1](http://www.w3.org/TR/CSS2/visudet.html#min-max-widths) で定義されている `0` に戻される形となり、CSS [フレキシブルボックス (flexbox)](https://developer.mozilla.org/ja/docs/Web/Guide/CSS/Flexible_boxes) の仕様が更新され、flexbox 上でも初期値が `0` となり、[`auto`](https://developer.mozilla.org/ja/docs/Web/CSS/auto) は正しい値とは見なされなくなりました。
