---
title: "NPN 対応が廃止されました"
date: "2017-02-06T19:16:00-05:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["53", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1248198"
      title: "Bug 1248198 - Drop NPN support"
---
Firefox 53 で、Next Protocol Negotiation (NPN) への対応が、代わりに [Application-Layer Protocol Negotiation](https://ja.wikipedia.org/wiki/Application-Layer_Protocol_Negotiation) (ALPN) を推奨する形で削除されました。2016 年 5 月に公開された [Chrome 51](https://developers.google.com/web/updates/2016/04/chrome-51-deprecations) で既に同様の変更が行われていることから、互換性への影響は軽微なはずです。
