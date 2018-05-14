---
title: "日本語版 Windows 7 で `<input>` の幅が広がっています"
date: "2015-08-16T03:30:08-04:00"
categories: ["html"]
tags: []
versions: ["40"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1194055"
      title: "Bug 1194055 - Size of <input> elements has changed in Firefox 40"
---
特定の環境、特に日本語版 Windows 7 において、[`<input>`](https://developer.mozilla.org/docs/Web/HTML/Element/input) フォームコントロール上で [`width`](https://developer.mozilla.org/docs/Web/CSS/width) が設定されていない場合にこの要素の幅が従来のバージョンよりも広がり、ページレイアウトが崩れる可能性のあることが分かりました。これは `<input>` 上の既定のフォントファミリー変更が原因です。Mozilla 開発者が解決策に取り組んでいる間、ウェブ開発者はこの要素に対して明示的に `width` あるいは [`font-family`](https://developer.mozilla.org/docs/Web/CSS/font-family) を指定することで問題を回避できます。

**更新**: この問題は <time datetime="2015-08-27">8 月 27 日</time> 公開の Firefox 40.0.3 で修正されました。
