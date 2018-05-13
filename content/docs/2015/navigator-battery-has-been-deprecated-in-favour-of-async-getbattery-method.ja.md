---
title: "`navigator.battery` が廃止予定となり、非同期 `getBattery` メソッドの使用が推奨されています"
date: "2015-09-13T23:41:00-04:00"
categories: ["dom"]
tags: []
versions: ["43"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1047119"
      title: "Bug 1047119 - Update Battery Status API to match latest Editors draft: navigator.getBattery(), etc"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1050749"
      title: "Bug 1050749 - Expose BatteryManager via getBattery() returning a Promise instead of a synchronous accessor (navigator.battery)."
aliases:
    - "/ja/docs/2015/navigator-battery-has-been-deprecated-in-favor-of-async-getbattery-method/"
---
[Battery Status API](https://developer.mozilla.org/docs/Web/API/Battery_Status_API) の実装が [最新の仕様](https://www.w3.org/TR/battery-status/) に合わせて更新されました。標準化された [`navigator.getBattery`](https://developer.mozilla.org/docs/Web/API/Navigator/getBattery) メソッドに置き換えられる形で [`navigator.battery`](https://developer.mozilla.org/docs/Web/API/Navigator/battery) プロパティが廃止予定となりました。この新しいメソッドは [`BatteryManager`](https://developer.mozilla.org/docs/Web/API/BatteryManager) インスタンスを得られる `Promise` を返します。`battery` プロパティ対応は将来的に削除されます。

**更新**: `navigator.battery` は [Firefox 50 で削除されました](https://www.fxsitecompat.com/ja/docs/2016/navigator-battery-has-been-removed-in-favour-of-async-getbattery-method/)。

**更新**: Battery Status API は [Firefox 52 で削除されました](https://www.fxsitecompat.com/ja/docs/2016/battery-status-api-has-been-removed/)。
