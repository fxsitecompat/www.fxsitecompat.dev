---
title: "`HTMLMediaElement.mozAutoplayEnabled` が削除されました"
date: "2017-11-15T10:46:00-05:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1336400"
      title: "Bug 1336400 - Remove HTMLMediaElement::mozAutoplayEnabled"
---
ブラウザー内でメディアの自動再生が有効になっているかどうかを返す、[`HTMLMediaElement`](https://developer.mozilla.org/ja/docs/Web/API/HTMLMediaElement) インターフェイス上の非標準 `mozAutoplayEnabled` 真偽値プロパティは、標準化されることがなかったため、Firefox 59 で削除されました。

自動再生機能は多くの場合ユーザー体験を損ねるため、基本的にウェブ開発者の皆さんはその使用を避けるべきです。それでも、その要素上の [`autoplay`](https://developer.mozilla.org/ja/docs/Web/API/HTMLMediaElement/autoplay) 属性の代わりにスクリプトを使用して、メディアの再生を開始することは可能です。
