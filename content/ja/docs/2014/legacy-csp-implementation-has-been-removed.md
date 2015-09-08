---
title: "古い CSP 実装が削除されました"
date: "2014-07-22T05:06:26-04:00"
categories: ["privacy-security"]
tags: []
versions: "33"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=949533": "Bug 949533 – Remove non-standard CSP parser and X-Content-Security-Policy header support"
---
Firefox 4 で初めて搭載された旧式の非標準 [Content Security Policy (CSP)](https://developer.mozilla.org/ja/docs/Web/Security/CSP) パーサが削除されました。これは Firefox 23 で標準の CSP 1.0 仕様が実装されたことに伴う措置で、接頭辞付き `X-Content-Security-Policy` ヘッダへの対応は打ち切られました。
