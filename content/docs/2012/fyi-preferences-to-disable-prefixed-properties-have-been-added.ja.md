---
title: "参考: 接頭辞付きプロパティを無効化する設定が追加されました"
date: "2012-12-03T03:54:45-05:00"
categories: ["css"]
tags: []
versions: ["19", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=804944"
      title: "Bug 804944 – add preferences for sets of CSS prefixed properties"
---
これはサイト互換性に影響を及ぼす変更ではありませんが、互換性を維持する取り組みの一環として開発されたもので、参考までに紹介します。いくつかの主要な接頭辞付きプロパティを無効化する設定が追加されました。`layout.css.prefixes.border-image`、`layout.css.prefixes.transforms`、`layout.css.prefixes.transitions`、`layout.css.prefixes.animations` の 4 つです。ウェブ開発者はこれらの設定を無効化する (値を `false` に変更する) ことで、接頭辞付き実装が削除された後も意図した通りにスタイルルールが反映されるかどうかをテストできます。詳しくは [David Baron のブログ記事](https://dbaron.org/log/20130225-removing-prefixes) を参照してください。
