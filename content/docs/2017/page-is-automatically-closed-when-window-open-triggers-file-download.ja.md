---
title: "`window.open()` でファイルのダウンロードが実行されるとページが自動的に閉じられてしまいます"
date: "2017-06-20T19:43:00-04:00"
categories: ["dom"]
tags: []
versions: ["54"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1373109"
      title: "Bug 1373109 - [e10s] window.open closes source page automatically after"
---
[`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) メソッドが PDF ドキュメントや ZIP アーカイブといったファイルのダウンロードに使われた場合、開かれているブラウザーのタブが予期せず閉じられてしまうというリグレッションが Firefox 54 で発生しました。Mozilla の開発者が解決策に取り組んでいます。ウェブ開発者には、`<a>` 要素上に HTML5 の `download` 属性を指定する方法で [ダウンロードリンクを作成する](https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks#Use_the_download_attribute_when_linking_to_a_download) ことをお勧めします。
