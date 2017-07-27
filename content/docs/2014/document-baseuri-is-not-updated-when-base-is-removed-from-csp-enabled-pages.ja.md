---
title: "CSP が有効になっているページから `<base>` が削除されたときに `document.baseURI` が更新されません "
date: "2014-10-17T22:50:44-04:00"
categories: ["dom"]
tags: []
versions: ["35"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1121857"
      title: "Bug 1121857 – document.baseURI does not get updated to document.location after base tag is removed from DOM for site with a CSP"
---
[`<base>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/base) 要素を使うと [`Node.baseURI`](https://developer.mozilla.org/ja/docs/Web/API/Node.baseURI) プロパティの値を変更することができます。この要素が削除されると、`baseURI` は自動的に規定値である [`document.location`](https://developer.mozilla.org/ja/docs/Web/API/document.location) に戻るはずですが、Firefox 35 では、ドキュメントの [CSP (Content Security Policy)](https://developer.mozilla.org/ja/docs/Web/Security/CSP) が有効になっている場合、復元が行われません。この問題は Firefox 35.0.1 で修正されました。
