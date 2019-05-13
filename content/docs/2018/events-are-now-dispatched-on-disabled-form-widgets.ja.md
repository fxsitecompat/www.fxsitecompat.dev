---
title: "無効化されたフォームウィジェット上でイベントが発生するようになりました"
date: "2018-12-20T23:22:00-05:00"
categories: ["dom"]
tags: []
versions: ["65"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=329509"
      title: "Bug 329509 - Do not prevent event dispatching even if there is no prescontext or (form) element is disabled"
---
Firefox 65 以降、`<input>`、`<textarea>`、`<button>`、`<select>` といったフォーム要素上で、それらが無効化されている場合にも標準や独自のイベントを発生させることが可能となりました。この変更は、ブラウザー間の相互運用性を改善させ、ウェブ開発者のニーズに応えることを目的としたものです。

要素が無効化されフォーカス不能なことから、`mousedown`、`mouseup`、`click`、`focus`、`input` といったほとんどのイベントは通常のユーザーインタラクションでは発生しませんが、`mouseover`、`mouseenter`、`mousemove`、`mouseout`、`mouseleave` は発生するようになります。これは Google Chrome、Apple Safari、Microsoft Edge の現行バージョンとは異なる点です。

意図せぬ挙動を防ぐため、イベントハンドラー内で処理を進める前に、必ずそのフォーム要素上の `disabled` プロパティを確認した方が良いでしょう。

**更新**: [Firefox 67](https://www.fxsitecompat.com/ja/docs/2019/css-animation-and-transition-events-are-now-fired-on-disabled-form-widgets/) 以降、CSS アニメーションとトランジション関連のイベントも、無効化された要素上で発生するようになりました。
