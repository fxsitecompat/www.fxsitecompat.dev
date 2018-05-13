---
title: "`cursor: -moz-zoom-in` と `-moz-zoom-out` の接頭辞が外れました"
date: "2013-05-19T07:35:00-04:00"
categories: ["css"]
tags: []
versions: ["24"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=772153"
      title: "Bug 772153 – unprefix CSS cursor: -moz-zoom-in | -moz-zoom-out"
---
[`cursor`](https://developer.mozilla.org/docs/Web/CSS/cursor) プロパティの値である [`-moz-zoom-in`](https://developer.mozilla.org/docs/Web/CSS/-moz-zoom-in) と [`-moz-zoom-out`](https://developer.mozilla.org/docs/Web/CSS/-moz-zoom-out) の接頭辞なし対応が追加されました。これらは元々 Mozilla の CSS 拡張仕様でしたが、現在は CSS3 UI エディターズドラフトの一部となっています。ある程度の期間が経過したら [接頭辞付きの値は削除されます](https://bugzilla.mozilla.org/show_bug.cgi?id=879119)。
