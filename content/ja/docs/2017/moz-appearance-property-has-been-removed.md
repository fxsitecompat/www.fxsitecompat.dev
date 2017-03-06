---
title: "`-moz-appearance` プロパティが廃止されました"
date: "2017-02-15T15:00:00-05:00"
categories: ["css"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1333482"
      title: "Bug 1333482 - [css-ui] Implement 'appearance:auto | none' and make -moz-appearance UA-sheet only"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/oZ9cPF8Y1pE/discussion"
      title: "Intent to implement and ship CSS 'appearance' with '-webkit-appearance' as an alias. Unship '-moz-appearance'."
---
Firefox 55 で、[`appearance`](https://developer.mozilla.org/ja/docs/Web/CSS/appearance) CSS プロパティへの対応が、WebKit/Blink 互換性のためのエイリアス `-webkit-appearance` とともに追加されました。一方、非標準の [`-moz-appearance`](https://developer.mozilla.org/ja/docs/Web/CSS/-moz-appearance) プロパティは、今後ウェブコンテンツ上では使用できなくなります。

`appearance:none` と `-webkit-appearance:none` はいずれも `-moz-appearance:none` と同じ働きをし、各要素のネイティブテーマを無効化します。初期値は `auto` です。
