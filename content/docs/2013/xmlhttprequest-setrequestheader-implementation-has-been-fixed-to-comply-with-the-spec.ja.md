---
title: "`XMLHttpRequest.setRequestHeader()` の実装が仕様に準拠するよう修正されました"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
releases: ["21", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=819051"
      title: "Bug 819051 – XMLHttpRequest.setRequestHeader() overwrites instead of combines values for the same header."
---
従来、[`XMLHttpRequest.setRequestHeader`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest#setRequestHeader) で同一のヘッダーが繰り返し指定されていた場合、最後に指定された値が使われていました。この挙動が仕様に準拠するよう修正され、それらの値が正しく連結されるようになりました。
