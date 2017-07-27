---
title: "文字列ではない値を返す JavaScript `src` を持った `<iframe>` 上で `load` イベントが発生しなくなりました"
date: "2016-10-16T01:05:00-04:00"
categories: ["dom", "javascript"]
tags: []
versions: ["49"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1268047"
      title: "Bug 1268047 - Change the handling of javascript: return values to align with other browsers and the updated spec"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1306472"
      title: "Bug 1306472 - No load event for iframe with javascript: URI that doesn't return a string"
---
Firefox 49 では、以下のように文字列を返さない JavaScript コードがソースの場合、`<iframe>` 要素上で [`load`](https://developer.mozilla.org/ja/docs/Web/Events/load) イベントが発生しません。

```html
<iframe src="javascript:true" onload="alert('hello')"></iframe>
```

この変更は最新の HTML 仕様に準拠するため行われたものですが、Firefox 49 のリリース後、正しく動作しないサイトがいくつか報告されています。そのため、この後方互換性のない変更は Firefox 49.0.2 で取り消され、従来通りイベントが発生するようになりました。
