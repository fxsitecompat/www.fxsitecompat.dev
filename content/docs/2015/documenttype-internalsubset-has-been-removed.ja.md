---
title: "`DocumentType.internalSubset` が削除されました"
date: "2015-10-20T15:37:00-07:00"
categories: ["dom"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=801545"
      title: "Bug 801545 - Remove obsolete attribute: DocumentType.internalSubset"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/u32smeY40Xw/discussion"
      title: "Intent to unship: DocumentType.internalSubset"
---
[`document.doctype`](https://developer.mozilla.org/docs/Web/API/Document/doctype) 上で参照できた古く無名の `DocumentType.internalSubset` プロパティが、DOM 仕様から除かれたため削除されました。
