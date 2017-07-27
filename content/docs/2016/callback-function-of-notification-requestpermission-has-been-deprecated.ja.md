---
title: "`Notification.requestPermission()` のコールバック関数が廃止予定となりました"
date: "2016-03-10T07:04:00-05:00"
categories: ["dom"]
tags: []
versions: ["46"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1241278"
      title: "Bug 1241278 - `Notification.requestPermission()` should return a promise"
---
[`Notification.requestPermission`](https://developer.mozilla.org/ja/docs/Web/API/Notification/requestPermission) メソッドの実装が最新の Notifications API 仕様に合わせて更新されました。このメソッドは許可設定の値をもたらす `Promise` を返すようになり、オプションのコールバック関数は廃止予定となりました。
