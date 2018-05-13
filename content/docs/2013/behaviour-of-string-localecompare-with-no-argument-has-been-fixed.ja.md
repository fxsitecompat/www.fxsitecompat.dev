---
title: "引数が指定されていない場合の `String.localeCompare` の挙動が修正されました"
date: "2013-02-06T08:44:10-05:00"
categories: ["javascript"]
tags: []
versions: ["21"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=789393"
      title: "Bug 789393 – String.prototype.localeCompare() with no argument always returns 0"
aliases:
    - "/ja/docs/2013/behaviour-of-string-localecompare-with-no-argument-has-been-fixed/"
---
[`String.localeCompare`](https://developer.mozilla.org/docs/JavaScript/Reference/Global_Objects/String/localeCompare) メソッドの実装が、最新の ECMAScript 5 仕様に準拠するよう更新されました。引数が何も渡されなかった場合、このメソッドは文字列 `"undefined"` を引数として取ります。
