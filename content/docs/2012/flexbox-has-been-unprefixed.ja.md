---
title: "Flexbox の接頭辞が外れました"
date: "2012-12-03T03:54:45-05:00"
categories: ["css"]
tags: []
versions: ["19", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=801098"
      title: "Bug 801098 – Unprefix CSS3 flexbox"
---
[CSS3 フレキシブルボックス (flexbox)](https://developer.mozilla.org/docs/CSS/Using_CSS_flexible_boxes) の接頭辞が外れました。今後、関連するプロパティやキーワードは `moz` 接頭辞なしで使用してください。なお Firefox 19 ではまだ flexbox が初期設定で無効化されています。この機能をテストしたい場合は `about:config` を開き `layout.css.flexbox.enabled` の値を `true` に変更する必要があります。
