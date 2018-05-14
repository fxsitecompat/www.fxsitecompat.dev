---
title: "999998 以上のグループを持つ正規表現が `InternalError` を投げるようになりました"
date: "2014-02-07T11:57:09-05:00"
categories: ["javascript"]
tags: []
versions: ["29"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=953013"
      title: "Bug 953013 – Regexp groups can overflow some counter"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=998785"
      title: "Bug 998785 – an error occurred while executing regular expression"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=976446"
      title: "Bug 976446 – Replace YARR with irregexp"
---
Firefox 29 以降、999998 上のグループを伴った [正規表現](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions) は動作しなくなり、「an error occurred while executing regular expression」という `InternalError` が投げられます。この変更は、カウンターがオーバーフローするのを防ぐことによって、パフォーマンスとセキュリティの改善を意図したものです。詳しくは [Egor Homakov のブログ記事](https://homakov.blogspot.ca/2013/12/regexp-groups-overflow-in-ff.html) を参照してください。

従来一致すべきなのに「一致なし」とされていた特定の正規表現が誤って `InternalError` につながるという、この変更によるリグレッションが報告されています。jQuery の旧バージョンに含まれる `trim` 関数も影響を受けることが判明しています。この問題は Firefox 30 で修正されました。
