---
title: "`x-moz-errormessage` 属性対応が廃止されました"
date: "2018-12-25T00:08:00-05:00"
categories: ["html"]
tags: []
versions: ["66"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1513890"
      title: "Bug 1513890 - Remove 'x-moz-errormessage' attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/LDNiOssSN3U/discussion"
      title: "Intent to unship: x-moz-errormessage attribute"
---
[フォームバリデーション](https://developer.mozilla.org/docs/Learn/HTML/Forms/Form_validation) に失敗したときに表示する任意のエラーメッセージを指定できるようにしていた HTML `<input>` 要素の非標準 `x-moz-errormessage` 属性への対応が Firefox 66 で廃止されました。標準の [`setCustomValidity`](https://developer.mozilla.org/docs/Web/API/HTMLSelectElement/setCustomValidity) メソッドで代用可能です。
