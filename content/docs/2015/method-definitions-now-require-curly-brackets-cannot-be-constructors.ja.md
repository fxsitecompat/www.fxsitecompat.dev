---
title: "メソッド定義に波括弧が必要となり、コンストラクターとして扱えなくなりました"
date: "2015-06-13T15:20:46-04:00"
categories: ["javascript"]
tags: []
versions: ["41"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1150855"
      title: "Bug 1150855 - Method definitions require curly brackets"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1059908"
      title: "Bug 1059908 - Method definitions and getter/setter functions should not be constructors"
---
これまで、[メソッド定義](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Functions/Method_definitions) の波括弧は必須ではありませんでした。Firefox 41 以降では、ECMAScript 6 仕様に従って波括弧は必須となり、付いていない場合は [`SyntaxError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError) が投げられます。同時に、ジェネレーターメソッドの例外を除き、メソッド定義をコンストラクターとして記述することはできなくなりました。
