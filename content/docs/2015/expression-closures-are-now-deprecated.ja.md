---
title: "式クロージャーが廃止予定となりました"
date: "2015-11-03T14:14:00-08:00"
categories: ["javascript"]
tags: []
versions: ["45"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=995610"
      title: "Bug 995610 – Add console warnings for expression closures (shorthand function syntax)"
---
JavaScript 1.8で導入された [式クロージャー](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Expression_closures) 構文が廃止予定となり、[近い将来削除されることとなりました](https://www.fxsitecompat.com/ja/docs/2015/expression-closure-support-will-be-removed/)。代わりに ECMAScript 6 [アロー関数](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Functions/Arrow_functions) 構文を使用してください。

**更新**: 式クロージャー対応は [Firefox 59 で廃止されました](https://www.fxsitecompat.com/ja/docs/2017/expression-closure-support-has-been-removed/)。
