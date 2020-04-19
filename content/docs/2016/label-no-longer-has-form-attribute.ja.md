---
title: "`<label>` の `form` 属性が廃止されました"
date: "2016-06-03T04:39:00-04:00"
categories: ["dom", "html"]
tags: []
releases: ["49", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1268852"
      title: "Bug 1268852 - Spec change: Remove <label form> and redefine label.form IDL attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/8TyeUQOn6qQ/discussion"
      title: "Intent to implement and ship: spec changes to the .form property and \"form\" attribute on <label> elements"
---
最新の HTML 仕様によれば、[`<label>`](https://developer.mozilla.org/docs/Web/HTML/Element/label) 要素はどの `<form>` とも関連付けられなくなりました。これを受けて、HTML5 で導入された `<label>` 上の `form` 属性への対応は Firefox 49 で削除されました。

一方で [`HTMLLabelElement`](https://developer.mozilla.org/docs/Web/API/HTMLLabelElement) DOM インスタンス上の `form` プロパティは、もしあればそのラベル付きコントロールの `form` プロパティを、なければ `null` を返すようになります。つまり、`label.form` は `label.control.form` のエイリアスとなります。
