---
title: "`line-height` が `<input>` にも適用されるようになりました"
date: "2014-03-21T04:50:04-04:00"
categories: ["css"]
tags: []
versions: ["30"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=349259"
      title: "Bug 349259 – CSS Property \'line-height\' has no effects on input text fields"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=697451"
      title: "Bug 697451 – Allow use of line-height for <input type=\"reset|button|submit\">"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1007454"
      title: "Bug 1007454 – Regression: Text on buttons on Ikea website are cut off"
---
これまで、Firefox は [`<input>`](https://developer.mozilla.org/docs/Web/HTML/Element/input) 要素上で指定された [`line-height`](https://developer.mozilla.org/docs/Web/CSS/line-height) プロパティを無視し、常に [`normal`](https://developer.mozilla.org/docs/Web/CSS/normal) を適用していました。一方 Internet Explorer や WebKit ベースのブラウザーではページ作者がこの値を増やすことが可能でした (ただし減らすことは不可)。相互運用性を改善するため、この挙動が変更され、作者が定義した値を受け入れるようになりました。後方互換性のため、1 行テキストの `<input>` にはこれまで通り `1` より小さい `line-height` を指定できません。

この変更によるリグレッションが、`line-height` が `1px` となっている *IKEA.com* で発見されていますが、これは意図した挙動と考えられています。
