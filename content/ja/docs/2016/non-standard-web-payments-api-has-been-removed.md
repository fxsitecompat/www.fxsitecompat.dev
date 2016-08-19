---
title: "非標準の Web Payments API が削除されました"
date: "2016-03-28T14:28:00-05:00"
categories: ["misc"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1252570"
      title: "Bug 1252570 - Remove mozPay"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/FvzDoaPGQ3g/discussion"
      title: "Intent to unship: navigator.mozPay - mozilla.dev.platform"
---
非標準の [Web Payments API](https://wiki.mozilla.org/WebAPI/WebPayment)、具体的には [`navigator.mozPay`](https://developer.mozilla.org/ja/docs/Web/API/Navigator/mozPay) メソッドへの対応が、Firefox 51 で削除されました。Web アプリケーション上での [アプリ内課金](https://developer.mozilla.org/ja/Marketplace/Monetization/In-app_payments_section/mozPay_iap) を実現するため Mozilla によって起草されたこの API は、当初 Firefox OS へ実装され、後に Android 版 Firefox やデスクトップ版 Firefox の [Web App Runtime](https://developer.mozilla.org/ja/Apps/Build/Architecture) でも有効化されましたが、広く普及することはありませんでした。Mozilla Marketplace の [課金対応は廃止予定](https://wiki.mozilla.org/Marketplace#Upcoming_Changes_to_Marketplace) であり、また既に Firefox 47 でデスクトップと Android から [Web App Runtime が削除されています](https://www.fxsitecompat.com/ja/docs/2016/web-app-runtime-has-been-removed-from-firefox-for-desktop-and-android/)。

将来的には、W3C の [Web Payments Working Group](https://www.w3.org/Payments/WG/) で設計が進んでいる標準の Web Payments API が Firefox に実装されるでしょう。
