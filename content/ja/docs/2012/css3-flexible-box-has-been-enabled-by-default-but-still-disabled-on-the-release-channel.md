---
title: "CSS3 可変ボックスが初期設定で有効になりましたが、まだ Release チャンネルでは無効化されています"
date: "2012-12-29T08:29:30-05:00"
categories: ["css"]
tags: []
versions: "20"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=783409": "Bug 783409 – Turn on CSS flexbox in builds by default (by enabling pref, build flag, etc)"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=841873": "Bug 841873 – Make flexbox automatically preffed off by default, in release builds"
---
[Firefox 18](https://developer.mozilla.org/ja/docs/Firefox_18_for_developers) で実装された新しい [可変ボックス (flexbox)](https://developer.mozilla.org/ja/docs/CSS/Using_CSS_flexible_boxes) が、隠し設定を変更することなく利用可能になりました。[`-moz-box-flex`](https://developer.mozilla.org/ja/docs/CSS/-moz-box-flex) など従来の接頭辞付き実装とは互換性がありませんので注意してください。

開発者の皆さんは [Aurora](http://www.mozilla.org/en-US/firefox/aurora/) または [Beta](http://www.mozilla.jp/firefox/beta/) で flexbox を試せるようになりましたが、**この機能は十分な品質が確保されるまで Release チャンネルでは引き続き無効化されます**。
