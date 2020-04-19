---
title: "CSS3 可変ボックスが初期設定で有効になりましたが、まだ Release チャンネルでは無効化されています"
date: "2012-12-29T08:29:30-05:00"
categories: ["css"]
tags: []
releases: ["20", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=783409"
      title: "Bug 783409 – Turn on CSS flexbox in builds by default (by enabling pref, build flag, etc)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=841873"
      title: "Bug 841873 – Make flexbox automatically preffed off by default, in release builds"
---
[Firefox 18](https://developer.mozilla.org/docs/Firefox_18_for_developers) で実装された新しい [可変ボックス (flexbox)](https://developer.mozilla.org/docs/CSS/Using_CSS_flexible_boxes) が、隠し設定を変更することなく利用可能になりました。[`-moz-box-flex`](https://developer.mozilla.org/docs/CSS/-moz-box-flex) など従来の接頭辞付き実装とは互換性がありませんので注意してください。

開発者の皆さんは [Aurora](https://www.mozilla.org/firefox/aurora/) または [Beta](https://www.mozilla.jp/firefox/beta/) で flexbox を試せるようになりましたが、**この機能は十分な品質が確保されるまで Release チャンネルでは引き続き無効化されます**。
