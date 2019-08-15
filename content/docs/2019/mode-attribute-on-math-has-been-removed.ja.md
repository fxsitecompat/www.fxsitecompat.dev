---
title: "`<math>` の `mode` 属性が削除されました"
date: "2019-08-15T10:45:00-04:00"
categories: ["misc"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1573438"
      title: "Bug 1573438 - Remove <math>'s mode attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/lZUF2Z9jOh4/discussion"
      title: "Intent to unship: <math>'s mode attribute"
---
[`<math>`](https://developer.mozilla.org/docs/Web/MathML/Element/math) 要素上の `mode` 属性への対応が Firefox 70 で廃止されました。この属性は、MathML 2 と Firefox 20 以降、`display` 属性に置き換えられる形で廃止予定となっていました。Firefox と Safari にしか実装されておらず、MathML 4 仕様から削除されます。古いドキュメント向けに [ポリフィル](https://github.com/mathml-refresh/mathml/issues/5#issuecomment-521525157) が公開されています。
