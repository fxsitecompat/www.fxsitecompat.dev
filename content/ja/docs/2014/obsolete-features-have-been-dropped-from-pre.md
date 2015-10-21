---
title: "`<pre>` から古い機能が削除されました"
date: "2014-02-07T11:57:09-05:00"
categories: ["html"]
tags: []
versions: ["29"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=949879": "Bug 949879 – Drop support for <pre cols>"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=950737": "Bug 950737 – Remove layout effect from <pre width>"
---
Firefox は [`<pre>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/pre) 要素の `cols`、`width` 両属性に対応しなくなりました。前者は Netscape Navigator 由来の非標準の拡張仕様でした。後者は HTML4 の仕様に含まれていましたが、[HTML5](https://developer.mozilla.org/ja/docs/Web/Guide/HTML/HTML5) から削除されました。
