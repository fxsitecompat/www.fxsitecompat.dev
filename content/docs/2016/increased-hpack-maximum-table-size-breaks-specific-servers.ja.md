---
title: "拡大された HPACK 最大テーブルサイズが特定のサーバーに影響しています"
date: "2016-10-07T00:55:00-04:00"
categories: ["networking"]
tags: []
releases: ["52", "52-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1296280"
      title: "Bug 1296280 - Change HPACK receive table size to 64k"
---
デスクトップ版の Firefox 52 で、HTTP/2 ヘッダー圧縮形式のひとつである HPACK の最大テーブルサイズが 4 KB から 64 KB へ変更されました。この新たな設定を適切に処理できない特定のウェブサーバーソフトウェアが確認されています。

バグ報告によれば、*Apache Tomcat* はバージョン 8.5.6 と 9.0.0.M11 でこの問題を修正しています。*Node.js SPDY Server* モジュールの 3.3.x にもバグがありますが、3.4.x には存在しないとのことです。これらのサーバーのいずれかを使用している場合は、この相互運用性問題を防ぐため、入手可能な最新版にアップグレードしてください。
