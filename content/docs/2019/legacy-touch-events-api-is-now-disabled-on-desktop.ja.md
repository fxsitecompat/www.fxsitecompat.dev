---
title: "デスクトップ上で旧式 Touch Events API が無効化されました"
date: "2019-05-12T23:43:00-04:00"
categories: ["dom"]
tags: []
releases: ["67", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1412485"
      title: "Bug 1412485 - Consider removing some parts of touch event APIs on desktop"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1500631"
      title: "Bug 1500631 - Consider removing document.createTouch and document.createTouchList"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/dwRNENReBuU/discussion"
      title: "Disabling document.createEvent(\"TouchEvent\"), document.createTouch* and ontouch* event handlers on desktop"
---
Firefox 67 は [Chrome 70](https://www.chromestatus.com/feature/4764225348042752) に続いてデスクトッププラットフォーム上で旧式の Touch Events API を無効化しました。これは [Firefox 52](https://www.fxsitecompat.dev/ja/docs/2016/touch-event-support-has-been-re-enabled-on-windows-desktop/) 以降使用可能となっていましたが、モバイル判別に誤用するサイトが後を絶たず、タッチスクリーンを備えたデスクトップパソコンやノートパソコン上で Firefox がモバイルブラウザーとして扱われてしまう場合があるためです。

これらは今後デスクトップ上で使用できなくなります。

* `document` 上の `createTouch`、`createTouchList`、`createEvent('TouchEvent')` メソッド
* `window`、`document`、`element` 上の `ontouchstart`、`ontouchmove`、`ontouchend`、`ontouchcancel` プロパティ

Touch Events API 自体はタッチスクリーン付きコンピューター上で引き続き使用可能です。これには以下のものが含まれます。

* `window` 上の `Touch`、`TouchEvent`、`TouchList` インターフェイス
* `addEventListener()` で使用可能な `touchstart`、`touchmove`、`touchend`、`touchcancel` イベントハンドラー

なお、`createTouch`、`createTouchList` 両メソッドは廃止予定となっており、近く Firefox から完全に削除されます。
