---
title: "`execCommand()` はコマンドが無効の場合に `false` を返すようになりました"
date: "2012-10-09T06:00:00-04:00"
categories: ["dom"]
tags: []
versions: ["16"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=760052": "Bug 760052 – execCommand() should return false if the command isn’t enabled"
---
[リッチテキストエディタ](https://developer.mozilla.org/ja/docs/Rich-Text_Editing_in_Mozilla) 上で使用される [`document.execCommand`](https://developer.mozilla.org/ja/docs/Web/API/document/execCommand) メソッドが、指定されたコマンドが有効でなければ正しく `false` を返すようになりました。これまでは常に `true` を返していました。
