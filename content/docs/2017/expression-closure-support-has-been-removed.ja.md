---
title: "式クロージャー対応が廃止されました"
date: "2017-12-26T10:51:00-05:00"
categories: ["javascript"]
tags: []
releases: ["60", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083458"
      title: "Bug 1083458 - Remove SpiderMonkey support for expression closures (shorthand function syntax)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1319512"
      title: "Bug 1319512 - Disable non-standard expression closure on nightly-only"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1426519"
      title: "Bug 1426519 - Disable non-standard expression closure everywhere"
aliases:
    - "/ja/docs/2015/expression-closure-support-will-be-removed/"
---
[Firefox 45 以降廃止予定となっていた](https://www.fxsitecompat.dev/ja/docs/2015/expression-closures-are-now-deprecated/) 非標準の [式クロージャー](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Expression_closures) (ショートハンド関数構文) は Firefox 60 で削除されました。代わりに標準の [アロー関数](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/Arrow_functions) 構文を使用してください。
