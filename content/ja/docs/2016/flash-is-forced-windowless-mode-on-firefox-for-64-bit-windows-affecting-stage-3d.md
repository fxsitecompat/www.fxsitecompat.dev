---
title: "64 ビット Windows 版 Firefox では Flash がウィンドウレスモード限定となり、Stage 3D が影響を受けます"
date: "2016-06-10T20:23:00-04:00"
categories: ["plugins"]
tags: []
versions: ["47"]
statuses: "affected"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1271398"
      title: "Bug 1271398 - [Regression] Problems with Adobe Flash Player Stage3D and Firefox x64 >=v47"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/EwI9Fq4DPy4/discussion"
      title: "Flash on Firefox Win64 runs on windowless mode only"
---
Firefox 47 以降、Windows 向け 64 ビット版 Firefox 上では、Adobe Flash Player プラグインはウィンドウレスモードのみで動作します。[`wmode=direct`](https://helpx.adobe.com/jp/flash/kb/231465.html#main_anc_c) は無視され、代わりに `wmode=opaque` が使用されます。この変更は、入力メソッド (IME) やファイルピッカーダイアログなど、いくつかのサンドボックス互換性問題を解決するために必要でした。

しかし、一部のインタラクティブな Flash コンテンツが、ウィンドウレスモード非対応の [Stage 3D](http://www.adobe.com/devnet/flashplayer/stage3d.html) API が使われているために動作しません。人気オンラインゲームの *Forge of Empires* が影響を受けることが判明しています。Firefox の 64 ビット版はまだ広く配布されていないことから、現時点で影響を受けるユーザは少数です。ゲーム開発者は Firefox ユーザに対して当面は 32 ビット版を推奨することが可能です。

バグのコメントによれば、ウィンドウレスモードで処理される新しいアクセラレーション描画モデルに対応した Flash Player Beta 向けに `wmode=direct` を再度有効化する計画があります。
