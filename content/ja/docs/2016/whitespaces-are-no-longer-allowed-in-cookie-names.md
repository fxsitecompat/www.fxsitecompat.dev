---
title: "Cookie の名前に空白文字を含めることはできなくなりました"
date: "2016-01-31T02:11:00-05:00"
categories: ["javascript", "networking"]
tags: []
versions: ["44"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1244505": "Bug 1244505 - Firefox 44 no longer allows spaces in cookie names, breaking some apps"
    "http://www.mozilla-japan.org/security/announce/2016/mfsa2016-04.html": "MFSA 2016-04 - Firefox で Cookie に制御文字を設定できてしまう問題"
---
これまで Firefox は、RFC 6265 に違反し、空白文字が [Cookie](https://developer.mozilla.org/ja/docs/Web/API/Document/cookie) の名前として保存されることを誤って許容していました。そうした実装ミスは Web サーバによる間違った Cookie 処理につながる恐れがあったことから、この挙動は中程度のセキュリティ問題と判断されました。

Firefox 44 でこの問題は修正され、不正な名前の Cookie は生成されなくなりました。JavaScript では、Cookie の名前と値は [`encodeURIComponent`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/encodeURIComponent) メソッドで事前にエンコードされなければなりません。
