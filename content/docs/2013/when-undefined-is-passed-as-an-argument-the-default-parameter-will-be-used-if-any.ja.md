---
title: "引数として `undefined` が渡された場合、デフォルト値が指定されていればそれが使われるようになりました"
date: "2013-01-03T03:53:26-05:00"
categories: ["javascript"]
tags: []
versions: ["18"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=781422"
      title: "Bug 781422 – parameters should get defaults whenever they are undefined"
---
[デフォルト引数](https://developer.mozilla.org/docs/JavaScript/Reference/default_parameters) は Firefox 15 で実装された ECMAScript 6 の機能ですが、従来は、引数として `undefined` が渡されたとき、その値が `undefined` となっていました。引数が渡されなかった場合と同様にデフォルト値になるよう、実装が変更されました。
