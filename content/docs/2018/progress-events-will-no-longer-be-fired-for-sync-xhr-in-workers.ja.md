---
title: "Worker 内の同期 XHR 上で `progress` イベントが発生しなくなりました"
date: "2018-09-06T01:36:00-04:00"
categories: ["dom"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1459984"
      title: "Bug 1459984 - Avoid firing an event named progress with synchronous XMLHttpRequest"
---
Firefox 63 以降、最新の `XMLHttpRequest` 仕様に従い、Worker 内部の同期リクエスト上では [`progress`](https://developer.mozilla.org/docs/Web/Events/progress) イベントが発生しなくなります。メインスレッド上では、少なくとも Firefox 52 以降この種類のイベントは発生していません。ダウンロードやアップロードの [進捗状況を監視](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/Using_XMLHttpRequest#Monitoring_progress) したい場合は、この変更の影響を受けない非同期リクエストを用いる必要があります。
