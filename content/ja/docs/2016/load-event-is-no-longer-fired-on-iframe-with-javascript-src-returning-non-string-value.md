---
title: "文字列ではない値を返す JavaScript `src` を持った `<iframe>` 上で `load` イベントが発生しなくなりました"
date: "2016-10-16T01:05:00-04:00"
categories: ["dom", "javascript"]
tags: []
versions: ["49"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1306472"
      title: "Bug 1306472 - No load event for iframe with javascript: URI that doesn't return a string"
---
Firefox 49 以降、以下のように文字列を返さない JavaScript コードがソースの場合、`<iframe>` 要素上で `load` イベントが発生しなくなります。

```html
<iframe src="javascript:true" onload="alert('hello')"></iframe>
```

この変更は最新の HTML 仕様に準拠するため行われたものですが、Firefox 49 のリリース後、正しく動作しないサイトがいくつか報告されています。このため、さらなる互換性問題を防ぐよう、Firefox 49.0.2 で従来の挙動に戻されました。
