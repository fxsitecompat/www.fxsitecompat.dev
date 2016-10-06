---
title: "Windows デスクトップ上でタッチイベント対応が再度有効となりました"
date: "2016-10-06T08:23:00-04:00"
categories: ["dom"]
tags: []
versions: ["52"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=806805"
      title: "Bug 806805 - [meta] Mouse / touch input problems on Windows devices that support touch input"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1180706"
      title: "Bug 1180706 - [meta] Touch support in APZ on desktop platforms"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1244402"
      title: "Bug 1244402 - Let touch events on windows ride the trains"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/4pPJfp_aSKE/discussion"
      title: "Touch events enabled on Windows desktop (nightly only)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6CGjsm1XpD4/discussion"
      title: "Intent to ship: TouchEvents (Windows), touch-action (all platforms), accessible caret"
---
[Firefox 18 で導入](https://www.fxsitecompat.com/ja/docs/2012/moztouch-events-were-removed-in-favour-of-the-standard-touch-events/) されたものの様々なサイト互換性問題のため [Firefox 24 で無効化](https://www.fxsitecompat.com/ja/docs/2013/touch-events-support-has-been-temporarily-disabled-on-desktop/) されていた、Windows デスクトッププラットフォーム上での標準 [タッチイベント](https://developer.mozilla.org/ja/docs/Web/API/Touch_events) 対応が、Firefox 52 で再び有効化されました。Firefox Nightly では Firefox 47 以降既に有効化されています。

バグの大半は Firefox もしくは当該サイトによって解決されていますが、まだ他に未報告の問題が存在する可能性があります。基本的に Web 開発者の皆さんは、ユーザがモバイル端末を使用しているかどうかの判別にタッチイベントを使用してはいけません。そうした場合、タッチパネル搭載のデスクトップパソコンやノートパソコン上で、あなたのサイトが予期せぬユーザ体験の問題を引き起こす恐れがあります。

簡単なテストを行うには、Firefox 開発者ツールの [レスポンシブデザインモード](https://developer.mozilla.org/ja/docs/Tools/Responsive_Design_Mode) を使って、タッチイベントをシミュレーションできます。
