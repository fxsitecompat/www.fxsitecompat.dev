---
title: "ホスト名が付かない URL は不正なものとして扱われるようになりました"
date: "2017-02-22T20:24:00-05:00"
categories: ["html", "networking"]
tags: []
versions: ["54"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1275746"
      title: "Bug 1275746 - Don't allow empty host name for URLTYPE_AUTHORITY URLs"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1305204"
      title: "Bug 1305204 - When trying to send/reply/forward an e-mail on webmail.earthlink.net I get a message \"Please enter a URL\""
---
Firefox 54 以降、`http:`、`http://`、`ftp:`、`ftp://` といったホスト名が指定されていない URL は、本来そうであるように、不正な URL として扱われるようになりました。つまり、以下の JavaScript コードは今後 `TypeError` を投げるようになります。

```js
new URL('http://')
```

また、このような URL 型の入力コントロールを含んだ HTML フォームは、値が手入力もしくは動的に変更されない限り、妥当とは見なされなくなります。

```html
<input type="url" value="http://">
```

この場合、`value` 属性を `placeholder` に置き換えることで問題を回避できます。
