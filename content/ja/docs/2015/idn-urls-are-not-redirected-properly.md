---
title: "IDN URL が適切にリダイレクトされません"
date: "2015-10-21T02:40:00-07:00"
categories: ["networking"]
tags: []
versions: ["36", "42"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1142083"
      title: "Bug 1142083 - IDN Unicode domain redirect is broken in Firefox 36/37/38"
---
Firefox 36 には、Unicode 形式の [国際化ドメイン名](https://ja.wikipedia.org/wiki/%E5%9B%BD%E9%9A%9B%E5%8C%96%E3%83%89%E3%83%A1%E3%82%A4%E3%83%B3%E5%90%8D) (IDN) を含む URL が適切にリダイレクトされず、「サーバが見つかりません」というエラーが表示されてしまうというリグレッションがあります。このバグは Firefox 41 で修正されましたが、まだ 42 以降には存在しています。

**更新**: このバグは Firefox 45 で再度修正されました。
