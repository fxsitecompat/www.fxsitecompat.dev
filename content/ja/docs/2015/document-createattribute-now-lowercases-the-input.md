---
title: "`document.createAttribute` が引数を小文字に変換するようになりました"
date: "2015-12-16T10:27:00-05:00"
categories: ["dom"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1176313"
      title: "Bug 1176313 - Make Attr follow the spec again"
---
[`document.createAttribute`](https://developer.mozilla.org/en-US/docs/Web/API/Document/createAttribute) メソッドの実装が最新の DOM 仕様に合わせて更新され、与えられた属性名を小文字に変換するようになりました。Mozilla の調査によれば、0.001% 未満の Web ページがこの変更による影響を受ける可能性があります。
