---
title: "`window.open()` の `dialog` オプションは非対応となりました"
date: "2015-10-06T00:25:00-04:00"
categories: ["dom"]
tags: []
versions: ["44", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1095236"
      title: "Bug 1095236 - [e10s] window.open(..., ..., \"dialog=1\") breaks with e10s enabled"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/cDpULPod8nQ/discussion"
      title: "mozilla.dev.platform: dialog=1 for window.open from content"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/gUORXMzvH1Y/discussion"
      title: "mozilla.dev.platform: Intent to unship: dialog=1 for window.open from web content"
---
[`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) メソッドの `dialog` オプションがウェブコンテンツから使用できなくなりました。この非標準機能は、最小化、最大化、復元ボタンをウィンドウのタイトルバーから取り除くものでしたが、Windows 版の Firefox とその他 Gecko ベースのブラウザーしか対応していませんでした。
