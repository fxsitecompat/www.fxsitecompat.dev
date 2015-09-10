---
title: "SSLv3 対応が削除されました"
date: "2015-03-17T14:02:59-04:00"
categories: ["privacy-security"]
tags: []
versions: "39"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1106470": "Bug 1106470 - Drop SSLv3 support entirely"
---
[Firefox 34 以降無効化されていた](https://www.fxsitecompat.com/ja/docs/2014/sslv3-has-been-disabled/) Mozilla 製品の SSL 3.0 対応が完全に削除されました。これは [このプロトコルがもはや安全とは言えないためです](https://blog.mozilla.org/security/2014/10/14/the-poodle-attack-and-the-end-of-ssl-3-0/)。Web サイトは代わりに TLS 1.2 を採用してください。
