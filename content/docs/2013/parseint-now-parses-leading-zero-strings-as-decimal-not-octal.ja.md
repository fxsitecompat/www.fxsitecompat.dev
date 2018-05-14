---
title: "`parseInt` が 0 で始まる文字列を 8 進数でなく 10 進数としてパースするようになりました"
date: "2013-02-06T08:44:10-05:00"
categories: ["javascript"]
tags: []
versions: ["21"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=786135"
      title: "Bug 786135 – Make parseInt(\"042\") === 42, now that other engines are moving that way"
---
[`parseInt`](https://developer.mozilla.org/docs/JavaScript/Reference/Global_Objects/parseInt) メソッドの実装が ECMAScript 5 仕様に準拠するよう更新され、0 で始まる文字列を 8 進数でなく 10 進数としてパースするようになりました。そのため、`parseInt("042")` は `34` の代わりに `42` を返すようになります。文字列を 8 進数としてパースしたい場合は、`parseInt(str, 8)` のように基数を指定してください。
