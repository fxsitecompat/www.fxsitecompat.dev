---
title: "`DOMError` が完全に削除されました"
date: "2019-06-17T18:30:00-04:00"
categories: ["dom"]
tags: []
versions: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1558387"
      title: "Bug 1558387 - Remove DOMError constructor"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6yQtQoNeR-s/discussion"
      title: "Intent to unship: DOMError"
---
非標準となり、すべてのインスタンスが `DOMException` に置き換えられた [Firefox 58](https://www.fxsitecompat.dev/ja/docs/2017/domerror-has-been-replaced-with-domexception/) 以降廃止予定となっていた `DOMError` インターフェイスが、Firefox 69 で削除されました。Mozilla の Telemetry によれば現在の使用率はほぼゼロであり、削除の互換性リスクは低いはずです。
