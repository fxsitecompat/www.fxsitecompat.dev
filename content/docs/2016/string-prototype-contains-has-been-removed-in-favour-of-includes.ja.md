---
title: "`String.prototype.contains` が `includes` に代わられ削除されました"
date: "2016-04-13T09:30:00-07:00"
categories: ["javascript"]
tags: []
versions: ["48"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1103588"
      title: "Bug 1103588 - Remove String.prototype.contains"
aliases:
    - "/ja/docs/2015/string-prototype-contains-will-be-removed/"
---
[Firefox 40 以降廃止予定となっていた](https://www.fxsitecompat.com/ja/docs/2015/string-prototype-contains-has-been-renamed-to-includes/) `String.prototype.contains` メソッドへの対応が削除されました。サイト互換性問題のため、このメソッドは [`String.prototype.includes`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/includes) に改名されました。
