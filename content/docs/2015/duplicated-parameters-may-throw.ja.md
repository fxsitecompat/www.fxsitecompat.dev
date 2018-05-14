---
title: "重複した引数が例外を投げる場合があります"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
versions: ["38"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1096376"
      title: "Bug 1096376 – Don\'t allow duplicate parameter names when rest-parameter is present"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1096377"
      title: "Bug 1096377 – Don\'t allow duplicate parameter names in arrow functions"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1096378"
      title: "Bug 1096378 – Don\'t allow duplicate parameter names in concise method definitions"
---
Firefox 38 以降、関数の重複した引数名が [残余引数](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/rest_parameters) (rest parameter) とともに、あるいは [アロー関数](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/Arrow_functions) や簡略メソッド定義で使われた場合に [`SyntaxError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError) が投げられます。
