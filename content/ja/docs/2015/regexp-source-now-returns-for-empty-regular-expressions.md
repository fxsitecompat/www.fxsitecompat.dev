---
title: "空の正規表現について `RegExp().source` が `\"(?:)\"` を返すようになりました"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
versions: ["38"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1130798"
      title: "Bug 1130798 – new RegExp().source should return \"(?:)\""
---
[`RegExp.prototype.source`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/RegExp/source) プロパティが、仕様に従って、正規表現が空の場合は空文字列の代わりに `"(?:)"` を返すようになりました。
