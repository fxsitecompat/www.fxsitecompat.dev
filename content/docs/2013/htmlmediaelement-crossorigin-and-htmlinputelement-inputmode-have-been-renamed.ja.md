---
title: "`HTMLMediaElement.crossorigin` と `HTMLInputElement.inputmode` が改名されました"
date: "2013-02-24T03:44:31-05:00"
categories: ["audio-video", "dom"]
tags: []
releases: ["22", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=847370"
      title: "Bug 847370 – HTMLMediaElement - crossOrigin vs crossorigin"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=850346"
      title: "Bug 850346 – inputmode vs inputMode for nsHTMLInputElement"
---
[`HTMLMediaElement`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) の `crossorigin` プロパティが `crossOrigin` に、[`HTMLInputElement`](https://developer.mozilla.org/docs/Web/API/HTMLInputElement) の`inputmode` プロパティが `inputMode` にそれぞれ改名されました。これは仕様に準拠するための変更です (大文字に注意)。
