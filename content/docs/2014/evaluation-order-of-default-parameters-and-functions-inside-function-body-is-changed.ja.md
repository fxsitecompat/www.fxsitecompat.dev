---
title: "デフォルト引数と関数本体内関数の評価順が変更されました"
date: "2014-07-22T05:06:26-04:00"
categories: ["javascript"]
tags: []
versions: ["33"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1022962"
      title: "Bug 1022962 – Default parameters should be evaluated before function declarations"
---
Firefox 15 で実装された [デフォルト引数](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/default_parameters) は、これまで関数本体内の関数の後に評価されていましたが、挙動が変更され、それらの関数の前に評価されるようになりました。そのため、デフォルト引数からそれらの関数を参照することはできなくなります。
