---
title: "`HTMLIFrameElement.sandbox` は `DOMSettableTokenList` を返すようになりました"
date: "2014-02-07T11:57:09-05:00"
categories: ["dom"]
tags: []
versions: "29"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=845057": "Bug 845057 – Fix the type of HTMLIFrameElement.sandbox"
---
従来、[`HTMLIFrameElement`](https://developer.mozilla.org/ja/docs/Web/API/HTMLIFrameElement) インタフェース ([`<iframe>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/iframe) 要素) の `sandbox` プロパティは `allow-same-origin` のような文字列値を返していました。最新の仕様に合わせ、この型が [`DOMSettableTokenList`](https://developer.mozilla.org/ja/docs/Web/API/DOMSettableTokenList) に変更されました。`sandbox.value` が従来と同じ文字列表現を返します。
