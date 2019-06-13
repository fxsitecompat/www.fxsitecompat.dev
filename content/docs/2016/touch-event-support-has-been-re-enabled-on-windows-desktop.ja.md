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
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1301327"
      title: "Bug 1301327 - Enabling `w3c_touch_events` on desktop Firefox is causing major problems with ExtJS6"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/4pPJfp_aSKE/discussion"
      title: "Touch events enabled on Windows desktop (nightly only)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6CGjsm1XpD4/discussion"
      title: "Intent to ship: TouchEvents (Windows), touch-action (all platforms), accessible caret"
---
[Firefox 18 で導入](https://www.fxsitecompat.dev/ja/docs/2012/moztouch-events-were-removed-in-favour-of-the-standard-touch-events/) されたものの様々なサイト互換性問題のため [Firefox 24 で無効化](https://www.fxsitecompat.dev/ja/docs/2013/touch-events-support-has-been-temporarily-disabled-on-desktop/) されていた、Windows デスクトッププラットフォーム上での標準 [タッチイベント](https://developer.mozilla.org/docs/Web/API/Touch_events) 対応が、Firefox 52 で再び有効化されました。Firefox Nightly では Firefox 47 以降既に有効化されています。

タッチパネル搭載端末では、[`Touch`](https://developer.mozilla.org/docs/Web/API/Touch)、[`TouchEvent`](https://developer.mozilla.org/docs/Web/API/TouchEvent)、[`TouchList`](https://developer.mozilla.org/docs/Web/API/TouchList) インターフェイスが、[`ontouchstart`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/ontouchstart)、[`ontouchmove`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/ontouchmove)、[`ontouchend`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/ontouchend)、[`ontouchcancel`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/ontouchcancel) プロパティとともに `window` 上に露呈されます。

以前報告された互換性問題の大半は Firefox もしくは当該サイトによって解決されていますが、まだ他に未報告のバグが存在する可能性があります。基本的にウェブ開発者の皆さんは、ユーザーがモバイル端末を使用しているかどうかの判別にタッチイベントを使用してはいけません。そうした場合、タッチパネル搭載のデスクトップパソコンやノートパソコン上で、あなたのサイトが予期せぬユーザー体験の問題を引き起こす恐れがあります。

```js
if ('ontouchstart' in window) {
  // これはモバイル判別ではなくタッチ判別です！
}
```

簡単なテストを行うには、Firefox 開発者ツールの [レスポンシブデザインモード](https://developer.mozilla.org/docs/Tools/Responsive_Design_Mode) を使って、タッチイベントをシミュレーションできます。タッチ判別の詳細は [この Mozilla Hacks の記事](https://hacks.mozilla.org/2013/04/detecting-touch-its-the-why-not-the-how/) を参照してください。

**更新**: この変更により現在 *Ext JS 6* が正しく動作していません。

**更新 2**: [Firefox 67](https://www.fxsitecompat.dev/ja/docs/2019/legacy-touch-events-api-is-now-disabled-on-desktop/) 以降、デスクトップ上で旧式の Touch Events API が無効化されています。
