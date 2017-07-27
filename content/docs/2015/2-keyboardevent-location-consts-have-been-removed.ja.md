---
title: "2 つの `KeyboardEvent` 位置定数が削除されました"
date: "2015-02-27T04:21:22-05:00"
categories: ["dom"]
tags: []
versions: ["38"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=936313"
      title: "Bug 936313 – Drop KeyboardEvent.DOM_LOCATION_MOBILE and KeyboardEvent.DOM_LOCATION_JOYSTICK of KeyboardEvent.location since they have been dropped from D3E spec"
---
`DOM_LOCATION_MOBILE`、`DOM_LOCATION_JOYSTICK` 両定数が、DOM3 Events 仕様から外れたため、[`KeyboardEvent`](https://developer.mozilla.org/ja/docs/Web/API/KeyboardEvent) インターフェイスから削除されました。
