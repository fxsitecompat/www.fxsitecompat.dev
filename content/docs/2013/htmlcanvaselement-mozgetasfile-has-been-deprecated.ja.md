---
title: "`HTMLCanvasElement.mozGetAsFile()` が廃止予定となりました"
date: "2013-09-19T23:58:13-04:00"
categories: ["canvas-webgl", "dom"]
tags: []
versions: ["26", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=803612"
      title: "Bug 803612 – Add deprecation warnings for mozGetAsFile"
---
[`HTMLCanvasElement`](https://developer.mozilla.org/docs/Web/API/HTMLCanvasElement) インターフェイス上の非標準の `mozGetAsFile` メソッドが廃止予定となり、近々削除されることになりました。代わりに標準の `toBlob` メソッドを使ってください。

**更新**: このメソッドは [Firefox 74](https://www.fxsitecompat.dev/ja/docs/2020/htmlcanvaselement-mozgetasfile-has-been-removed/) で廃止されました。
