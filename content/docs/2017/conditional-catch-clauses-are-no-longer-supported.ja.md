---
title: "条件付き `catch` 節への対応が打ち切られました"
date: "2017-11-15T11:49:00-05:00"
categories: ["javascript"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1228841"
      title: "Bug 1228841 - Remove support for conditional catch expressions"
aliases:
    - "/ja/docs/2015/conditional-catch-clause-support-will-be-removed/"
---
非標準の [条件付き `catch` 節](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/try...catch#Conditional_catch_clauses) への対応は Firefox 59 で削除されました。MDN の記事で説明されている通り、標準の [`if...else`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/if...else) 命令文で代用してください。他のブラウザーには実装されたことがないため、互換性リスクは非常に低いはずです。
