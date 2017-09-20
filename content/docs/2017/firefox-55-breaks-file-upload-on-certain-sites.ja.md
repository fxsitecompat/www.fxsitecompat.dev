---
title: "Firefox 55 では特定のサイトでファイルアップロードが機能しません"
date: "2017-08-22T13:24:00-04:00"
categories: ["dom"]
tags: []
versions: ["55"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1383518"
      title: "Bug 1383518 - Uploading thumbnails to YouTube, picture to Tweakers.net not working on Firefox 55+"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1393063"
      title: "Bug 1393063 - XHR send of FormData with certain Blobs hangs indefinitely (Firefox 55.0.0 - 55.0.2)"
---
アップロードストリームの処理方法の変更が原因で、ウェブフォームからのファイルのアップロードが特定の状況で機能せず、サーバーからのレスポンスが 400 Bad Request エラーになってしまう場合があるというリグレッションが Firefox 55 で発生しました。Ajax 形式のフォームを提供している *YouTube* で動画のサムネイルをアップロードできないという報告がユーザーから上がっていますが、静的なフォームも影響を受ける可能性があります。Mozilla の開発者が解決策に取り組んでいます。

**更新**: Service Worker に関係するバグであることが判明したこのリグレッションは Firefox 55.0.3 で修正されました。しかし Firefox 55 には、Service Worker がなくても特定の `Blob` を伴う [`FormData`](https://developer.mozilla.org/ja/docs/Web/API/FormData) を用いた非同期 `XMLHttpRequest` や `fetch` が失敗するという、アップロードに関するもうひとつのリグレッションがあります。Mozilla 開発者はこのバグにも取り組んでいます。

**更新 2**: `FormData` のリグレッションは Firefox 56 で修正されました。
