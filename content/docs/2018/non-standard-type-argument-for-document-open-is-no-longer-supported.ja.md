---
title: "`document.open()` の非標準 `type` 引数対応が廃止されました"
date: "2018-06-03T21:42:00-04:00"
categories: ["dom"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1444872"
      title: "Bug 1444872 - Remove processing for document.open()'s type parameter"
---
Firefox は、[`document.open`](https://developer.mozilla.org/docs/Web/API/Document/open) メソッドについて、`type`、`replace` という 2 つの非標準オプション引数に対応しています。Firefox 61 以降、`type` は無視され、常に `text/html` が新たに開かれたドキュメントの MIME タイプとして使われるようになります。これらの引数には他のどのブラウザーも対応していないことから、互換性リスクは非常に低いはずです。
