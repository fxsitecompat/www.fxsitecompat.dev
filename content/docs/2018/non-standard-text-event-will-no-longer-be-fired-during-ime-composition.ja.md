---
title: "非標準 `text` イベントが IME 変換中に発生しなくなりました"
date: "2018-11-30T02:45:00-05:00"
categories: ["dom"]
tags: []
versions: ["65"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1288640"
      title: "Bug 1288640 - Stop dispatching \"text\" event in web contents"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/2pw2HxiCIbc/discussion"
      title: "Intent to unship: DOM \"text\" event"
---
Firefox 65 以降、ウェブコンテンツ上で非標準の `text` DOM イベントが発生しなくなりました。これはブラウザーのエディター UI にインプットメソッドエディター (IME) 変換中の文字列データや選択範囲を通知するために実装されたもので、内部での使用のみ想定したものでした。文書化されておらず他のどのブラウザーも対応していないことから、互換性リスクは非常に低いはずです。
