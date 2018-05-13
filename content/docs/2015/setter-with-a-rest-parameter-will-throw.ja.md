---
title: "残余引数付きのセッターが例外を投げるようになります"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
versions: ["38"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1089632"
      title: "Bug 1089632 – Setter with a RestParameter should be a SyntaxError"
---
[残余引数](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/rest_parameters) (rest parameter) が付いた [セッター](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/set) が、仕様に従って [`SyntaxError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError) を投げるようになりました。
