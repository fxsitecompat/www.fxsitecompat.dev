---
title: "古い CSS スクロールスナップ構文対応が廃止されました"
date: "2019-05-28T05:04:00-04:00"
categories: ["css"]
tags: []
versions: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1312163"
      title: "Bug 1312163 - Update 'scroll-snap-type' to the latest specification and drop support for 'scroll-snap-type-x' and 'scroll-snap-type-y'"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1544136"
      title: "Bug 1544136 - Ship the new scroll snap"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/s0rMvOBnO_4/discussion"
      title: "Intent to implement and ship the CSS Scroll Snap Module Level 1 and unship old scroll snap properties"
---
Firefox 68 で [最新の CSS スクロールスナップ仕様](https://drafts.csswg.org/css-scroll-snap-1/) が実装されました。この仕様は Firefox 39 で [初期実装](https://hacks.mozilla.org/2015/09/scroll-snapping-explained/) が行われてから大幅に改定されました。Chrome と Safari は既に新しい構文への対応を追加していますが、Firefox で行われた変更には後方互換性がありません。

* `scroll-snap-coordinate`、`scroll-snap-destination`、`scroll-snap-type-x`、`scroll-snap-type-y` プロパティは削除されました
* `scroll-snap-type` プロパティはロングハンドとなったため、`scroll-snap-type:mandatory` のような古いショートハンド構文は動かなくなります

もし既にスクロールスナップを活用している場合は、新しい構文に合わせて適宜スタイルシートを更新してください。
