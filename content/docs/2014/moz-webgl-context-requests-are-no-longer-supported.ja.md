---
title: "`moz-webgl` コンテキストリクエストが廃止されました"
date: "2014-02-07T11:57:09-05:00"
categories: ["canvas-webgl"]
tags: []
versions: ["29", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=913597"
      title: "Bug 913597 – Remove support for \'moz-webgl\' context requests"
---
[Canvas](https://developer.mozilla.org/docs/HTML/Canvas) から古い `moz-webgl` の名前を使って [WebGL](https://developer.mozilla.org/docs/Web/WebGL) コンテキストを取得する方法は対応が打ち切られました。[Getting started with WebGL](https://developer.mozilla.org/docs/Web/WebGL/Getting_started_with_WebGL#Creating_a_WebGL.C2.A0context) で説明されているように、標準の `webgl` コンテキストを使ってください。
