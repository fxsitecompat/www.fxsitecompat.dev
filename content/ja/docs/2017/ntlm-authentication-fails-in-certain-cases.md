---
title: "NTLM 認証が HTTPS サイトに対して失敗する場合があります"
date: "2017-03-14T20:40:00-04:00"
categories: ["networking"]
tags: []
versions: ["52"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1346392"
      title: "Bug 1346392 - Firefox 52.0 fails to NTLM authenticate to SharePoint Server 2016 sites over TLS 1.2"
---
TLS 1.2 を通じて配信され [NTLM 認証](https://ja.wikipedia.org/wiki/NT_LAN_Manager) を必要とするサイトへユーザーがログインできないというリグレッションが Firefox 52 で発生しました。報告されたアプリケーションは *SharePoint Server 2016* ですが、他のサイトも影響を受ける可能性があります。

Microsoft による調査によれば、NTLM は HTTP/2 と互換性がないにも関わらず、Firefox が認証時に接続を HTTP/1.1 へダウングレードしないことが原因です。

Mozilla 開発者が解決策を模索しています。当面の間、[`about:config`](https://support.mozilla.org/t5/Manage-preferences-and-add-ons/Firefox-%E3%81%AE-Configuration-Editor/ta-p/33503) を通じて隠し設定 `network.http.spdy.enabled.http2` を切り替え、HTTP/2 を一時的に無効化することで問題を回避できます。
