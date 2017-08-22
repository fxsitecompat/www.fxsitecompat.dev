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
---
アップロードストリームの処理方法の変更が原因で、ウェブフォームからのファイルのアップロードが特定の状況で機能せず、サーバーからのレスポンスが 400 Bad Request エラーになってしまう場合があるというリグレッションが Firefox 55 で発生しました。Ajax 形式のフォームを提供している *YouTube* で動画のサムネイルをアップロードできないという報告がユーザーから上がっていますが、静的なフォームも影響を受ける可能性があります。Mozilla の開発者が解決策に取り組んでいます。
