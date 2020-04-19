---
title: "ホスト名が付かない URL は不正なものとして扱われるようになりました"
date: "2017-02-22T20:24:00-05:00"
categories: ["html", "networking"]
tags: []
releases: ["54", "60-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1275746"
      title: "Bug 1275746 - Don't allow empty host name for URLTYPE_AUTHORITY URLs"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1305204"
      title: "Bug 1305204 - When trying to send/reply/forward an e-mail on webmail.earthlink.net I get a message \"Please enter a URL\""
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1373327"
      title: "Bug 1373327 - Sending mails from earthlink webmail account stopped working in Firefox 54"
---
Firefox 54 以降、`http:`、`http://`、`ftp:`、`ftp://` といったホスト名が指定されていない URL は、本来そうであるように、不正な URL として扱われるようになりました。つまり、以下の JavaScript コードは今後 `TypeError` を投げるようになります。

```js
new URL('http://')
```

また、このような URL 型の入力コントロールを含んだ HTML フォームは、値が手入力もしくは動的に変更されない限り、妥当とは見なされなくなります。

```html
<input type="url" value="http://">
```

この場合、`value` 属性を `placeholder` 属性に置き換えることで問題を回避できます。

**更新**: *EarthLink Web Mail* がこの変更の影響を受けており、顧客がメッセージを送信できない状態となっています。
