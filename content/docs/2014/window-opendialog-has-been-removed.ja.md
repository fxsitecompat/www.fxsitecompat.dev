---
title: "`window.openDialog` が削除されました"
date: "2014-06-09T02:46:54-04:00"
categories: ["dom"]
tags: []
versions: ["32"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=962747"
      title: "Bug 962747 – Hide Window.openDialog from content"
---
非標準メソッド [`window.openDialog`](https://developer.mozilla.org/docs/Web/API/window.openDialog) がウェブコンテンツから使用できなくなりました。代わりに [`window.open`](https://developer.mozilla.org/docs/Web/API/window.open) を使用してください。
