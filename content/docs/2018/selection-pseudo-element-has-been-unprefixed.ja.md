---
title: "`::selection` 疑似要素の接頭辞が外れました"
date: "2018-05-10T12:36:00-04:00"
categories: ["css"]
tags: []
releases: ["62", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=509958"
      title: "Bug 509958 - Remove the -moz prefix from ::selection"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/dQVpQYjn3-M/discussion"
      title: "Intent to unprefix: ::-moz-selection."
---
[`::selection`](https://developer.mozilla.org/docs/Web/CSS/::selection) 疑似要素の接頭辞が Firefox 62 で外れました。Firefox はベンダー接頭辞を保っている唯一の主要ブラウザーでした。廃止予定となった `::-moz-selection` はまだエイリアスとして使用できますが、将来的に削除されます。
