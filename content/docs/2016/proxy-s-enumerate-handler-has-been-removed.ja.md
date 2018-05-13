---
title: "`Proxy` の `enumerate` ハンドラーが削除されました"
date: "2016-02-14T03:53:00-05:00"
categories: ["javascript"]
tags: []
versions: ["47"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1246318"
      title: "Bug 1246318 - Remove [[Enumerate]] and associated reflective capabilities"
---
[`for-in`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...in) 命令文を捕捉するため [`Proxy`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy) 内で使われていた [`handler.enumerate`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy/handler/enumerate) メソッドが、ECMAScript 2016 (ES7) 仕様と Firefox 47 から削除されました。
