---
title: "`X-Frame-Options: Allow-From` ディレクティブが削除されました"
date: "2019-10-08T17:17:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
releases: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1301529"
      title: "Bug 1301529 - Misleading console message for X-Frame-Options Allow-From mismatch (remove X-Frame-Options: allow-from)"
---
時代遅れとなった [`X-Frame-Options`](https://developer.mozilla.org/docs/Web/HTTP/Headers/X-Frame-Options) HTTP レスポンスヘッダー用の `allow-from` ディレクティブへの対応が Firefox 70 で廃止されました。これはまだ Internet Explorer を含む古いブラウザー向けには有効ですが、モダンブラウザー向けに `Content-Security-Policy` (CSP) ヘッダーの [`frame-ancestors`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy/frame-ancestors) ディレクティブを併用すべきです。
