---
title: "`navigator` オブジェクトの `geolocation` プロパティが API 無効化時に存在しなくなりました"
date: "2013-07-14T19:12:37-04:00"
categories: ["dom"]
tags: []
versions: ["25"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=884921"
      title: "Bug 884921 – Align navigator.geolocation with spec"
---
[Geolocation API](https://developer.mozilla.org/docs/WebAPI/Using_geolocation) 実装が標準準拠のために更新されました。この機能が利用できない場合、[`window.navigator.geolocation`](https://developer.mozilla.org/docs/Web/API/window.navigator.geolocation) は `null` の代わりに `undefined` を返すようになり、`"geolocation" in navigator` は従来の `true` の代わりに `false` を返します。
