---
title: "`:active` 疑似クラスがテキストボックスに反映されません"
date: "2015-10-21T02:20:00-07:00"
categories: ["css"]
tags: []
versions: ["38", "38-esr"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1168055"
      title: "Bug 1168055 - Active Pseudo class not working for textbox in firefox 38"
---
Firefox 38 には [`:active`](https://developer.mozilla.org/docs/Web/CSS/:active) CSS 疑似クラスが [`<input>`](https://developer.mozilla.org/docs/Web/HTML/Element/input) や [`<textarea>`](https://developer.mozilla.org/docs/Web/HTML/Element/textarea) 要素に反映されないというリグレッションがあります。このバグは Firefox 39 で修正されました。
