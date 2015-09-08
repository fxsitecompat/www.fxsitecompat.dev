---
title: "`MozTouch` イベントが廃止され、標準のタッチイベントに置き換えられました"
date: "2012-12-03T03:53:26-05:00"
categories: ["dom"]
tags: []
versions: "18"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=726615": "Bug 726615 – Support W3C touch event instead of MozTouch event"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=798821": "Bug 798821 – Disable touch events on Windows for devices that do not support touch input"
---
Firefox の試験実装で廃止予定となっていた [`MozTouch*` API](https://developer.mozilla.org/ja/docs/DOM/Touch_events_%28Mozilla_experimental%29) (`MozTouchDown`、`MozTouchMove`、`MozTouchUp` イベント) が削除されました。今後は [W3C 標準のタッチイベント](https://developer.mozilla.org/ja/docs/DOM/Touch_events) を使用してください。

サイト互換性を確保するため、Windows ではタッチ入力の可否を自動判別し、非対応端末ではタッチイベントを無効化するようになりました。上記バグのコメントによれば、対応端末は現時点でわずか数パーセントとのことです。Android では初期設定で有効となっています。Mac 版と Linux 版の Firefox ではまだタッチイベントが実装されていません。

**多くのサイトで [タッチイベントに関する互換性問題](https://bugzilla.mozilla.org/showdependencytree.cgi?id=806805&hide_resolved=1) が確認されています**。既にサイトやアプリケーション側でモバイル向けの対応を行っている場合は、Firefox をはじめとするデスクトップブラウザでも期待通りに動作するかどうか必ずテストしましょう。
