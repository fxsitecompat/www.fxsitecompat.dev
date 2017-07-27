---
title: "`<body>` 上のマージン属性対応がすべてのモードに拡大されました"
date: "2014-10-17T22:50:44-04:00"
categories: ["html"]
tags: []
versions: ["35"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=95530"
      title: "Bug 95530 – topmargin and leftmargin attributes on the BODY element should be honored in all modes (not just Quirks mode)"
---
これまで Internet Explorer との互換性のため [Quirks (後方互換) モード](https://developer.mozilla.org/ja/docs/Mozilla_Quirks_Mode_Behavior) のみの対応となっていた [`<body>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/body) 要素の非標準属性、`topmargin`、`bottommargin`、`rightmargin`、`leftmargin` が、HTML5 仕様に取り入れられたため、Standards (標準準拠) モードでも反映されるようになりました。
