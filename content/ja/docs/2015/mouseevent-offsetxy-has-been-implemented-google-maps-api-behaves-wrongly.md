---
title: "`MouseEvent.offsetX`/`Y` が実装されましたが、Google Maps API の誤動作が確認されています "
date: "2015-07-13T10:05:10-04:00"
categories: ["dom"]
tags: ["regression"]
versions: "39"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=69787": "Bug 69787 - Implement MSIE\'s event.offsetX, event.offsetY as mouse coordinates inside target element"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1175863": "Bug 1175863 - Google Maps API V3 drawing manager bug"
    "https://groups.google.com/d/topic/mozilla.dev.platform/ibv6l2-LG3E/discussion": "Intent to ship: MouseEvent.offsetX/Y"
---
MSIE 由来の [`MouseEvent.offsetX`](https://developer.mozilla.org/ja/docs/Web/API/MouseEvent/offsetX)、[`MouseEvent.offsetY`](https://developer.mozilla.org/ja/docs/Web/API/MouseEvent/offsetY) 両プロパティが CSSOM View 仕様で標準化され、ついに Firefox にも実装されました。この変更により、[Google Maps API の Drawing Layer におけるバグ](https://code.google.com/p/gmaps-api-issues/issues/detail?id=8278) が露呈しており、おそらく不適切なユーザエージェント判別が原因で、結果的に誤ったマウス座標が返されるという問題が発生しています。Google が修正に取り組んでいます。

**更新**: Google はまだ修正を行っていませんが、バグの [コメント](https://bugzilla.mozilla.org/show_bug.cgi?id=1175863#c24) によれば、Maps API のスクリプト URL に `v=3` を付加することで問題を回避できるそうです。
