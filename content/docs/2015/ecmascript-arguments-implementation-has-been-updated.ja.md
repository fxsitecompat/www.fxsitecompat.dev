---
title: "ECMAScript `arguments` 実装が更新されました"
date: "2015-09-24T17:00:00-04:00"
categories: ["javascript"]
tags: []
versions: ["43"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=889158"
      title: "Bug 889158 - Calling an arrow function shouldn't create an 'arguments' binding"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1175394"
      title: "Bug 1175394 - Mapped arguments object should only be created when its FormalParameters is a SimpleParameterList"
---
ECMAScript 2015 (ES6) 準拠の一環として、[アロー関数](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/Arrow_functions) は自身の [`arguments`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/arguments) を持たなくなりました。`arguments` オブジェクトは今後、もしあれば外側の関数から継承される形になります。[残余引数](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/rest_parameters) 構文を使えば、アロー関数の実際の引数にアクセスできます。

また、Firefox 43 以降、*マップされた* `arguments` オブジェクトは、そのコードが非 [strict モード](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Strict_mode) 内にあり、なおかつその関数が残余引数、[デフォルト引数](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/Default_parameters)、[分割代入引数](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#Function_argument_defaults) のいずれも持たない場合にのみ提供されます。MDN ドキュメント上の [例](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/arguments#Rest_default_and_destructured_parameters) を参照してください。
