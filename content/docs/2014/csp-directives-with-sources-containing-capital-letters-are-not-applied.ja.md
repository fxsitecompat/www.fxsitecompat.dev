---
title: "大文字を含むソースの CSP ディレクティブが適用されません "
date: "2014-10-17T22:50:44-04:00"
categories: ["privacy-security"]
tags: []
versions: ["35"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1122445"
      title: "Bug 1122445 – CSP change in behavior regards case sensitivity loading resources"
---
Firefox 35 では、[Content Security Policy (CSP)](https://developer.mozilla.org/docs/Web/Security/CSP) のソース URL に `https://www.example.com/OnlineBanking` のように大文字が含まれている場合、そのディレクティブが適用されません。Firefox の現行 CSP 実装はソース URL を内部で小文字に変換しており、そのために実際の URL と一致しないことが Mozilla 開発者によって確認されました。この問題は Firefox 35.0.1 で修正されました。
