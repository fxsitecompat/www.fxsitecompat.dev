---
title: "`Node.attributes` が削除されました"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
versions: ["22", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=844134"
      title: "Bug 844134 – attributes should be defined on Element and not Node"
---
[`Node.attributes`](https://developer.mozilla.org/docs/Web/API/Node.attributes) プロパティは、仕様から削除されたため、使用できなくなりました。[`Element.attributes`](https://developer.mozilla.org/docs/Web/API/Element.attributes) プロパティは引き続き使用可能です。
