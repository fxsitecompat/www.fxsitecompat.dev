---
title: "`CSS` インターフェイスの型が `function` から `object` へ変わりました"
date: "2018-05-07T21:30:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1455805"
      title: "Bug 1455805 - Make \"CSS\" a namespace, not interface"
---
CSS ワーキンググループ内での [議論](https://github.com/w3c/csswg-drafts/pull/437) の結果、[`CSS`](https://developer.mozilla.org/ja/docs/Web/API/CSS) インターフェイスが内部的には名前空間となりました。この変更に伴い、`typeof CSS` は `"function"` の代わりに `"object"` を返すようになったため、これを用いて機能判別を実装する際には注意が必要です。

```js
// これは今後動作しません
if (typeof CSS === 'function' && typeof CSS.supports === 'function') {
  // CSS.supports が使用可能
}

// 書き換え例 1
if (typeof CSS !== 'undefined' && typeof CSS.supports === 'function')

// 書き換え例 2
if ('CSS' in window && typeof CSS.supports === 'function')
```
