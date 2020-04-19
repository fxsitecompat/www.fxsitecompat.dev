---
title: "`DataView.length` が `3` から `1` に変わりました"
date: "2018-12-21T04:02:00-05:00"
categories: ["javascript"]
tags: []
releases: ["65", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1334813"
      title: "Bug 1334813 - Should DataView.length be 1 ?"
---
[`DataView`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/DataView) コンストラクター上の `length` プロパティはこれまで ECMAScript 6 草案通り `3` でした。これが、Firefox 65 以降、最新の仕様に従って `1` となります。現時点で他の一部のブラウザーはまだ `3` を返す可能性があります。
