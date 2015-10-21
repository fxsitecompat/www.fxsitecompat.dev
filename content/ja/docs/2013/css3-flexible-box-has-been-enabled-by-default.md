---
title: "CSS3 可変ボックスが初期設定で有効となりました"
date: "2013-02-24T03:44:31-05:00"
categories: ["css"]
tags: []
versions: ["22"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=841876": "Bug 841876 – Re-enable flexbox pref (by default) in release builds"
---
[Firefox 18](https://developer.mozilla.org/ja/docs/Firefox_18_for_developers) で実装された新しい [可変ボックス (flexbox)](https://developer.mozilla.org/ja/docs/Web/Guide/CSS/Flexible_boxes) が、隠し設定を変更せずに使用可能となりました。なお、これは [`-moz-box-flex`](https://developer.mozilla.org/ja/docs/Web/CSS/-moz-box-flex) のような従来の接頭辞付き実装とは互換性がないことに注意してください。
