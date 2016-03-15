---
title: "`Navigator.requestWakeLock` が Firefox OS 以外で無効化されました"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
versions: ["30"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=963366"
      title: "Bug 963366 – Hide navigator.requestWakeLock and MozWakeLock from the web except on Firefox OS"
---
[Power Management API](https://developer.mozilla.org/ja/docs/WebAPI/Power_Management) の一部である [`Navigator.requestWakeLock`](https://developer.mozilla.org/ja/docs/Web/API/Navigator.requestWakeLock) メソッドと [`MozWakeLock`](https://developer.mozilla.org/ja/docs/Web/API/MozWakeLock) オブジェクトは、Firefox OS のみで役立つものの、すべてのプラットフォームで有効になっていました。これらは今後 Firefox OS 以外では無効となります。
