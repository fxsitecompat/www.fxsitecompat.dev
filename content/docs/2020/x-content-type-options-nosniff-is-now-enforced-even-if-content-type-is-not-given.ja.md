---
title: "`Content-Type` 未指定の場合も `X-Content-Type-Options:nosniff` が遵守されるようになりました"
date: "2020-02-12T23:28:00-05:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["75"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1594766"
      title: "Bug 1594766 - Decide whether to continue ignoring XCTO Nosniff when Content Type is Empty, or to enforce"
    - url: "https://blog.mozilla.org/security/2020/04/07/firefox-75-will-respect-nosniff-for-page-loads/"
      title: "Firefox 75 will respect ‘nosniff’ for Page Loads | Mozilla Security Blog"
---
[Firefox 72](https://www.fxsitecompat.dev/ja/docs/2019/x-content-type-options-nosniff-now-applies-to-top-level-documents-causing-some-pages-to-be-downloaded/) 以降、[`X-Content-Type-Options`](https://developer.mozilla.org/docs/Web/HTTP/Headers/X-Content-Type-Options) HTTP レスポンスヘッダーはトップレベルドキュメントにも適用されていますが、互換性リスクを緩和するため、`Content-Type` ヘッダーが空だったり指定されていない場合は `nosniff` ディレクティブは無視されていました。

Mozilla の Telemetry によって実際のリスクがないことが証明されたため、この回避策は Firefox 75 で削除されました。ただ、サーバーやアプリケーションの誤設定が原因で、この `nosniff` 遵守により HTML ページがダウンロードされる状態が引き起こされるため、ウェブ開発者の皆さんはこの変更について知っておくべきでしょう。
