---
title: "`line-height:-moz-block-height` への対応が廃止されました"
date: "2019-05-28T04:06:00-04:00"
categories: ["css"]
tags: []
releases: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1540093"
      title: "Bug 1540093 - Unship line-height: -moz-block-height."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/XA2mqBeNrk4/discussion"
      title: "Intent to Unship: -moz-block-height value for line-height"
---
CSS `line-height` プロパティの非標準 `-moz-block-height` 値がウェブコンテンツから使用できなくなりました。これは行高を外側のブロックの高さに合わせることを可能にするものでしたが、本来 Firefox 内部での使用のみ意図していました。他のどのブラウザーにも実装されていないことから、互換性リスクは非常に低いはずです。
