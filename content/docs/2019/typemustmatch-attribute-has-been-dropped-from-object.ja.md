---
title: "`<object>` の `typemustmatch` 属性が廃止されました"
date: "2019-05-28T00:20:00-04:00"
categories: ["dom", "html"]
tags: []
versions: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1548773"
      title: "Bug 1548773 - Remove support for typemustmatch"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6dOIeUcHY6g/discussion"
      title: "Intent to unship: typeMustMatch attribute on <object> elements"
---
HTML `<object>` 要素上の `typemustmatch` 属性とそれに対応する `HTMLObjectElement` DOM インターフェイス上の [`typeMustMatch`](https://developer.mozilla.org/docs/Web/API/HTMLObjectElement/typeMustMatch) プロパティへの対応が最新の HTML Living Standard と Firefox 68 から削除されました。他のどのブラウザーもこの属性に対応していないため、互換性リスクは非常に低いはずです。
