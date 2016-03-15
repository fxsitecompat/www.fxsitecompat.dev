---
title: "複雑なアプリが内部 JavaScript エラーを投げる場合があります "
date: "2014-07-22T05:06:26-04:00"
categories: ["javascript"]
tags: []
versions: ["33"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083913"
      title: "Bug 1083913 – Switch statement too large internal error"
---
WebGL ベースのゲームのような複雑な Web アプリケーションが、Firefox の従来のバージョンでは見られなかった内部 JavaScript エラーを投げる可能性があります。このリグレッションはソースマップ対応の改善に起因するもので、Firefox 34 で修正されます。
