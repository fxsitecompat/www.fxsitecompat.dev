---
title: "`KeyboardEvent.DOM_VK_ENTER` が削除されました"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
versions: ["30", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=969247"
      title: "Bug 969247 – Get rid of related code of NS_VK_ENTER and nsIDOMKeyEvent::DOM_VK_ENTER"
---
[`KeyboardEvent`](https://developer.mozilla.org/docs/Web/API/KeyboardEvent) インターフェイスから `DOM_VK_ENTER` 定数が削除され、`14` の代わりに `null` を返すようになりました。この定数は [keydown`](https://developer.mozilla.org/docs/Web/Reference/Events/keydown) や [`keypress`](https://developer.mozilla.org/docs/Web/Reference/Events/keypress) といったキーイベントで一度も使われたことがないため、既存のコードには影響しないはずですが、もしコードに含まれている場合は削除した方が良いでしょう。`DOM_VK_RETURN` が <kbd>Enter</kbd>、<kbd>Return</kbd> 両キーを表します。
