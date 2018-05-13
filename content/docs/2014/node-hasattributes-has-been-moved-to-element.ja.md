---
title: "`Node.hasAttributes` が `Element` へ移動されました"
date: "2014-10-17T22:50:44-04:00"
categories: ["dom"]
tags: []
versions: ["35"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1055773"
      title: "Bug 1055773 – Move hasAttributes() to Element"
---
廃止予定となっていた `hasAttributes` メソッドが [`Node`](https://developer.mozilla.org/docs/Web/API/Node) インターフェイスから削除されました。[`Element.hasAttributes`](https://developer.mozilla.org/docs/Web/API/Element.hasAttributes) メソッドが同じ機能を提供するので、この変更は一般的な使用事例には影響しないはずです。
