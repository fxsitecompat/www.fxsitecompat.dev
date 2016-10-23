---
title: "旧式ジェネレーター関数がメソッド定義内で許容されなくなりました"
date: "2016-08-08T08:58:00-04:00"
categories: ["javascript"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1199296"
      title: "Bug 1199296 - Don't allow legacy generator yield in method definitions"
---
従来、[メソッド定義](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Functions/Method_definitions) のゲッター内で [`yield`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/yield) キーワードを用いることで、それを暗黙のうちに [旧式ジェネレーター関数](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/Legacy_generator_function) とすることが可能でした。そのような構文は現在の ECMAScript 仕様によれば妥当でないため、Firefox は `SyntaxError` を投げるようになりました。[このニュースグループへの投稿](https://groups.google.com/d/topic/firefox-dev/2AklfAAFQuw/discussion) で説明されている通り、代わりに [ジェネレーターメソッド](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Functions/Method_definitions#Shorthand_generator_methods) を使用してください。
