---
title: "`:-moz-table-border-nonzero` 擬似クラスが削除されました"
date: "2017-02-28T23:43:00-05:00"
categories: ["css"]
tags: []
versions: ["54", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1341925"
      title: "Bug 1341925 - Restrict :-moz-table-border-nonzero pseudo-class to UA stylesheet"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/jtdC_pUmCew/discussion"
      title: "Intent to unship: \"-moz-table-border-non-zero\" pseudo-class outside UA stylesheet"
---
非標準で文書化されていない `<table>` 要素用 `:-moz-table-border-nonzero` 擬似クラスがウェブコンテンツ上で使用できなくなりました。代わりとなるセレクタは `[border]:not([border="0"])` です。
