---
title: "`HTMLMediaElement.srcObject` の接頭辞が外れました"
date: "2015-08-05T00:48:18-04:00"
categories: ["audio-video", "dom"]
tags: []
versions: "42"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1175523": "Bug 1175523 - Unprefix mozSrcObject (to srcObject)"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1183495": "Bug 1183495 - Remove mozSrcObject alias to srcObject soon"
---
[`HTMLMediaElement`](https://developer.mozilla.org/ja/docs/Web/API/HTMLMediaElement) インタフェース上の [`srcObject`](https://developer.mozilla.org/ja/docs/Web/API/HTMLMediaElement/srcObject) プロパティの接頭辞が外れました。接頭辞付き `mozSrcObject` プロパティはエイリアスとして残されていますが、近々削除されます。
