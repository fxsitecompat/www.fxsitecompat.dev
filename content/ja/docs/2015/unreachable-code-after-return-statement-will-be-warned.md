---
title: "`return` 命令文に続く到達不能コードに警告が表示されるようになりました"
date: "2015-04-27T13:17:23-04:00"
categories: ["javascript"]
tags: []
versions: ["40"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1005110": "Bug 1005110 - Warn about unreachable code after semicolon-less return statement"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1151931": "Bug 1151931 - Warning for \"unreachable expression after semicolon-less return statement\" triggers incorrectly (braceless if, ASI)"
---
[Web コンソール](https://developer.mozilla.org/ja/docs/Tools/Web_Console) が、[`return`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/return) 命令文の後の到達不能コードに警告を表示するようになりました。これには　[改行と戻り値になり得る値が後に続く return 命令文](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/return#Automatic_semicolon_insertion) といったよくある誤解を招きやすいコーディングスタイルが含まれます。
