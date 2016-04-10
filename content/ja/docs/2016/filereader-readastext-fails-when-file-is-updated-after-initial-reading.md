---
title: "ファイルが初回読み取り後に更新された場合 `FileReader.readAsText` が動作しません"
date: "2016-04-06T18:19:00-04:00"
categories: ["dom"]
tags: []
versions: ["45"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1260606"
      title: "Bug 1260606 - FileReader.readAsText(HTML_FORM_INPUT.files[0]) fails on content size change"
---
[`FileReader.readAsText`](https://developer.mozilla.org/ja/docs/Web/API/FileReader/readAsText) メソッドでファイルを読み込んだ後、ファイルの内容が変更され、それを再度読み込もうとした場合にエラーが投げられるというリグレッションが Firefox 45 で発生しました。ファイルサイズが変わらない場合、この問題は発生しません。Mozilla 開発者が解決策に取り組んでいます。
