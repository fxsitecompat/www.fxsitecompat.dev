---
title: "`-moz-binding` CSS プロパティが廃止されました"
date: "2019-05-13T03:25:00-04:00"
categories: ["css"]
tags: []
versions: ["67"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1523712"
      title: "Bug 1523712 - Restrict parsing of -moz-binding to chrome and UA sheets."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/TR1_24OldK8/discussion"
      title: "Intent to unship: -moz-binding CSS property from content."
---
現在では廃止予定となっている XML Binding Language (XBL) を要素と結び付けるため Firefox 内部で使用することを意図していた `-moz-binding` CSS プロパティがウェブコンテンツから使用できなくなりました。以前はウェブ上で Firefox を対象とした CSS ハックに使用可能でしたが、Firefox 67 以降では無視されます。
