---
title: "`DocumentTouch` が削除されました"
date: "2013-07-14T19:12:37-04:00"
categories: ["dom"]
tags: []
versions: ["25", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=897211"
      title: "Bug 897211 – Remove nsIDOMDocumentTouch"
---
[`DocumentTouch`](https://developer.mozilla.org/docs/Web/API/DocumentTouch) インターフェイスが、仕様の廃止に伴って削除されました。[`createTouch`](https://developer.mozilla.org/docs/Web/API/DocumentTouch.createTouch)、[`createTouchList`](https://developer.mozilla.org/docs/Web/API/DocumentTouch.createTouchList) 両メソッドは [`Document`](https://developer.mozilla.org/docs/Web/API/Document) インターフェイスへ移動されました。
