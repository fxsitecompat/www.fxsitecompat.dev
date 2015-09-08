---
title: "デバッガ有効時に `eval` 内のコードが動作しません "
date: "2014-03-21T04:50:04-04:00"
categories: ["javascript"]
tags: ["regression"]
versions: "30"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=998908": "Bug 998908 – [jsdbg2] Calling Debugger.Script.prototype.getChildScripts causes errors to be thrown that otherwise wouldn\'t be"
---
JavaScript エンジンのリグレッションにより、Firefox 内で [デバッガ](https://developer.mozilla.org/ja/docs/Tools/Debugger) もしくは [Firebug](https://getfirebug.com/) 拡張機能が有効化されている場合、[`eval`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/eval) 内部のスクリプトの一部が正しく動作せず `ReferenceError` を投げる可能性があります。この問題は特に ExtJS や Google Maps API に影響しており、[Firefox Aurora もしくは Beta](http://www.mozilla.jp/firefox/preview/) を使用することで回避できます。
