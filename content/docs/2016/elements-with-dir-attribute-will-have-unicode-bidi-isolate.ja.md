---
title: "`dir` 属性付き要素に `unicode-bidi:isolate` が適用されます"
date: "2016-03-07T11:46:00-05:00"
categories: ["css", "html"]
tags: []
versions: ["47"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1218706"
      title: "Bug 1218706 - Make unicode-bidi: isolate the default for elements with a dir attribute"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1249497"
      title: "Bug 1249497 - Make bdo element use unicode-bidi: isolate-override"
---
HTML5 仕様で `dir` 属性の意味が変更され、[`<bdo>`](https://developer.mozilla.org/docs/Web/HTML/Element/bdo) 要素上では [`unicode-bidi`](https://developer.mozilla.org/docs/Web/CSS/unicode-bidi)`:bidi-override` の代わりに `unicode-bidi:isolate-override` を、それ以外のすべての要素では `unicode-bidi:embed` の代わりに `unicode-bidi:isolate` を使うこととなりました。

Firefox のユーザーエージェントスタイルシートも仕様に従うため更新されましたが、`<bdo>` ではまだ `unicode-bidi:bidi-override` が使用されています。この不一致は近く修正されます。Firefox 47 以降では、他の要素には `unicode-bidi:-moz-isolate` が適用されます。

**更新**: Firefox 50 以降では `<bdo>` 要素に `unicode-bidi:isolate-override` が適用されます。
