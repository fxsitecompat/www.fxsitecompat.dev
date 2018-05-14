---
title: "複数のルールが指定された場合に `CSSStyleSheet.insertRule` が例外を投げるようになりました"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
versions: ["21"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=765599"
      title: "Bug 765599 – CSSStyleSheet.insertRule should throw when there are more than one rule"
---
複数のルールが [`CSSStyleSheet.insertRule`](https://developer.mozilla.org/docs/Web/API/CSSStyleSheet/insertRule) メソッドに渡された場合、最初のルールだけがスタイルシートに挿入されていました。今後 Firefox は他のブラウザーと同様に例外 `SYNTAX_ERR` を投げます。
