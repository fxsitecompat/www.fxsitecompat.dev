---
title: "`xml:base` 属性対応が廃止されました"
date: "2018-12-24T23:47:00-05:00"
categories: ["misc"]
tags: []
versions: ["66"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=903372"
      title: "Bug 903372 - Remove support for xml:base"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/goHxC7z3D7Q/discussion"
      title: "Intent to unship xml:base"
---
[Firefox 53](https://www.fxsitecompat.dev/ja/docs/2017/xml-base-attribute-has-been-deprecated/) 以降廃止予定となっていた [`xml:base`](https://www.w3.org/TR/xmlbase/) 属性への対応が Firefox 66 で削除されました。 HTML [`<base>`](https://developer.mozilla.org/docs/Web/HTML/Element/base) 要素に似たこの機能は何年も前に仕様から削除されており、現時点で他のどのブラウザーも対応していないため、削除のリスクは非常に低いはずです。
