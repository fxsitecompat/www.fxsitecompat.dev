---
title: "`Node.getUserData()` と `setUserData()` が削除されました"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
versions: ["22"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=842372"
      title: "Bug 842372 – Make getUserData and setUserData ChromeOnly"
---
[`Node.getUserData`](https://developer.mozilla.org/docs/Web/API/Node.getUserData)、[`Node.setUserData`](https://developer.mozilla.org/docs/Web/API/Node.setUserData) 両メソッドがウェブコンテンツから使用できなくなりました。[`Element.dataset`](https://developer.mozilla.org/docs/Web/API/Element.dataset) もしくは [`WeakMap`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) で代用してください。
