---
title: "無効化されたフォームウィジェット上で CSS アニメーションとトランジション関連のイベントが発生するようになりました"
date: "2019-05-12T21:29:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["67"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1530239"
      title: "Bug 1530239 - css transition events must fire even if an element is disabled"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1531605"
      title: "Bug 1531605 - css animation events must fire even if an element is disabled"
---
Firefox 67 以降、`animationend` や `transitionend` などの CSS アニメーション、トランジション関連イベントが、`<input>`、`<textarea>`、`<button>`、`<select>` といったフォーム要素上で、それらが無効化されている場合にも発生するようになりました。

そうした要素上でマウスイベントの発生を可能にした、[Firefox 65](https://www.fxsitecompat.com/ja/docs/2018/events-are-now-dispatched-on-disabled-form-widgets/) で行われた類似の変更と同様に、予期せぬ挙動を防ぐためイベントハンドラー内で `disabled` プロパティを確認した方が良いかもしれません。
