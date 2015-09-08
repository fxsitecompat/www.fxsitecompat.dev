---
title: "`PushManager.hasPermission` が削除されました"
date: "2015-08-05T00:48:18-04:00"
categories: ["dom"]
tags: []
versions: "42"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1183853": "Bug 1183853 - Rename hasPermission() to permissionState()"
---
廃止予定となっていた [`hasPermission`](https://developer.mozilla.org/ja/docs/Web/API/PushManager/hasPermission) メソッドが、標準化された [`permissionState`](https://developer.mozilla.org/ja/docs/Web/API/PushManager/permissionState) メソッドに置き換えられる形で [`PushManager`](https://developer.mozilla.org/ja/docs/Web/API/PushManager) インタフェースから削除されました。
