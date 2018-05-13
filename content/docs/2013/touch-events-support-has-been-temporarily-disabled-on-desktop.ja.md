---
title: "タッチイベント対応がデスクトップで一時的に無効化されました"
date: "2013-05-19T07:35:00-04:00"
categories: ["dom"]
tags: []
versions: ["24"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=888304"
      title: "Bug 888304 – Content touch-events on Firefox-desktop should be disabled until we can support them properly"
---
[Firefox 18 で導入された](https://www.fxsitecompat.com/ja/docs/2012/moztouch-events-were-removed-in-favour-of-the-standard-touch-events/) [タッチイベント](https://developer.mozilla.org/docs/Web/Guide/API/DOM/Events/Touch_events) 対応が**デスクトップ版** Firefox で無効化されました。*Google* や *Twitter* といった一部の人気サイトが正常に動作していないことが確認されたためです。バグが修正され次第、この API は再度有効化されます。強制的に有効化するには、`about:config` を開き `dom.w3c_touch_events.enabled` の設定値を `2` に変更してください。[Firefox for Android](https://developer.mozilla.org/docs/Mozilla/Firefox_for_Android) と [Firefox OS](https://developer.mozilla.org/docs/Mozilla/Firefox_OS) を含むモバイル版はこの変更を受けません。また、この API は Windows 8 向けの Metro スタイル Firefox では有効化されています。
