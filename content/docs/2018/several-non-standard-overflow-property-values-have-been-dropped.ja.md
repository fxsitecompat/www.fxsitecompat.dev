---
title: "いくつかの非標準 `overflow` プロパティ値が廃止されました"
date: "2018-08-14T14:08:00-04:00"
categories: ["css"]
tags: []
releases: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1481125"
      title: "Bug 1481125 - Tracking -moz-scrollbars-none when creating webcompat issues."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/rujif05uOTo/discussion"
      title: "Intent to unship: overflow: -moz-scrollbars-* values"
---
以下に挙げる非標準の接頭辞付き [`overflow`](https://developer.mozilla.org/docs/Web/CSS/overflow) CSS プロパティ値が、標準の値に置き換えられる形で、初期設定により無効化されました。

* `-moz-scrollbars-none`
    * `overflow: hidden` で代用してください
* `-moz-scrollbars-horizontal`
    * `overflow-x: scroll; overflow-y: hidden` で代用してください
    * <del>[Firefox 63 以降](https://www.fxsitecompat.dev/ja/docs/2018/overflow-shorthand-syntax-has-been-updated-to-swap-2-values/) では `overflow: hidden scroll` も使用可能です</del>
* `-moz-scrollbars-vertical`
    * `overflow-x: hidden; overflow-y: scroll` で代用してください
    * <del>[Firefox 63 以降](https://www.fxsitecompat.dev/ja/docs/2018/overflow-shorthand-syntax-has-been-updated-to-swap-2-values/) では `overflow: scroll hidden` も使用可能です</del>

これにより `-moz-hidden-unscrollable` がこのプロパティの唯一の接頭辞付き値となります。ただしこれは一般用ではありません。
