---
title: "Latin-1 のみの文字列に対する正規表現がパフォーマンス問題を引き起こす場合があります "
date: "2014-07-22T05:06:26-04:00"
categories: ["javascript"]
tags: []
versions: ["33"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1081175": "Bug 1081175 – (latin1strings) Degraded regular expression performance (infinite loop?)"
---
Firefox 33 では、Latin-1 文字列のみで表現される文字列に対する正規表現操作が非常に遅く、ハングにつながる場合もあります。このリグレッションは [内部文字エンコーディングの変更](https://blog.mozilla.org/javascript/2014/07/21/slimmer-and-faster-javascript-strings-in-firefox/) に起因するもので、Firefox 34 で修正されます。
