---
title: "`HTMLMediaElement.src` の種類が変更されました"
date: "2012-12-03T03:50:54-05:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["17"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=792665": "Bug 792665 – Separate HTMLMediaElement.src from HTMLMediaElement.srcObject"
---
従来 [`HTMLMediaElement`](https://developer.mozilla.org/ja/docs/DOM/HTMLMediaElement) の `src` プロパティの値はメディアストリームのオブジェクトとなっていました。標準化にあたって、`src` プロパティはメディアの URL 文字列とし、オブジェクトは別途新たな `srcObject` プロパティに含めるという提案を Mozilla が行い、Firefox の実装はそれにそった形に変更されました。今のところ `srcObject` は接頭辞付きの `mozSrcObject` となっています。
