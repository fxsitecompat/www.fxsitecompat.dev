---
title: "Quirks モードで `:active` と `:hover` がリンクのみに適用されるようになりました"
date: "2014-12-19T11:15:21-05:00"
categories: ["css"]
tags: []
versions: ["36"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=783213"
      title: "Bug 783213 – :active and :hover quirk should only apply to links"
---
従来、ページが [Quirks (後方互換) モード](https://developer.mozilla.org/ja/docs/Mozilla_Quirks_Mode_Behavior) でレンダリングされる場合、[`:active`](https://developer.mozilla.org/ja/docs/Web/CSS/:active)、[`:hover`](https://developer.mozilla.org/ja/docs/Web/CSS/:hover) 両疑似クラスは、リンクだけでなく画像や [フォームコントロール](https://developer.mozilla.org/ja/docs/Web/Guide/HTML/Forms_in_HTML) にも適用可能でした。こうした挙動が仕様や他のブラウザーに合わせる形で修正されました。この変更に関する詳細は [バグのコメント](https://bugzilla.mozilla.org/show_bug.cgi?id=783213#c31) を参照してください。
