---
title: "予約語の関数名への使用は許容されなくなりました"
date: "2013-09-19T23:58:13-04:00"
categories: ["javascript"]
tags: []
versions: ["26", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=907958"
      title: "Bug 907958 – Restrict function names to non-keywords"
---
[予約語](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Reserved_Words) を関数名に使用することはできません。Firefox 26 以降、そうしたコードは [`SyntaxError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError) を投げます。例えば `function delete() { ... }` は不正な構文です。
