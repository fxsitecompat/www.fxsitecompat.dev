---
title: "`hasFeature` が SVG の場合にも常に `true` を返すようになります"
date: "2016-09-06T22:24:00-04:00"
categories: ["dom", "svg"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=984778"
      title: "Bug 984778 - Make hasFeature() always return true (even for SVG)"
---
[Firefox 19](https://www.fxsitecompat.com/ja/docs/2012/hasfeature-issupported-methods-now-always-return-true/) 以降、[`document.implementation.hasFeature`](https://developer.mozilla.org/docs/Web/API/DOMImplementation/hasFeature) メソッドは SVG 機能を除き `true` を返しています。Firefox 51 でこの例外が廃止されることとなり、今後は引数が無視され常に `true` が返されるようになります。Google Chrome が 2015 年 7 月公開のバージョン 44 以降すでに `true` を返していることから、互換性への影響は軽微なはずです。
