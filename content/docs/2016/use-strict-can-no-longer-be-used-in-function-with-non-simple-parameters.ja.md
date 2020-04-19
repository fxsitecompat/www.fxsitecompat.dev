---
title: "単純でない引数を伴った関数内で `use strict` を使用できなくなります"
date: "2016-10-25T10:28:00-04:00"
categories: ["javascript"]
tags: []
releases: ["52", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1272784"
      title: "Bug 1272784 - |function f(a = 1) { \"use strict\"; }| should throw Early Error."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/jAWMy-W_AaY/discussion"
      title: "Intent to unship: Use strict in function with non-simple parameters"
---
ECMAScript 2016 仕様によれば、[strict モード](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Strict_mode) を発動させる `"use strict";` 命令文を [デフォルト引数](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/Default_parameters) や [残余引数](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/rest_parameters) を伴った関数内で使用することはできません。Firefox 52 以降ではそうしたコードに対して `SyntaxError` が投げられます。Google Chrome と Microsoft Edge がすでにこの変更を行っていることから、互換性への影響は軽微なはずです。
