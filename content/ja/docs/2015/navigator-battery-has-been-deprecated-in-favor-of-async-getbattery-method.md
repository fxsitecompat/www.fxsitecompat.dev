---
title: "`navigator.battery` が廃止予定となり、非同期 `getBattery` メソッドの使用が推奨されています"
date: "2015-09-13T23:41:00-04:00"
categories: ["dom"]
tags: []
versions: ["43"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1047119": "Bug 1047119 - Update Battery Status API to match latest Editors draft: navigator.getBattery(), etc"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1050749": "Bug 1050749 - Expose BatteryManager via getBattery() returning a Promise instead of a synchronous accessor (navigator.battery)."
---
[Battery Status API](https://developer.mozilla.org/ja/docs/Web/API/Battery_Status_API) の実装が [最新の仕様](http://www.w3.org/TR/battery-status/) に合わせて更新されました。標準化された [`navigator.getBattery`](https://developer.mozilla.org/ja/docs/Web/API/Navigator/getBattery) メソッドに置き換えられる形で [`navigator.battery`](https://developer.mozilla.org/ja/docs/Web/API/Navigator/battery) プロパティが廃止予定となりました。この新しいメソッドは [`BatteryManager`](https://developer.mozilla.org/ja/docs/Web/API/BatteryManager) のための [`Promise`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Promise) を返します。`battery` プロパティ対応は将来的に削除されます。
