---
title: "Firefox 47 Beta と 48 Developer Edition が公開されました"
date: "2016-04-30T12:38:00-04:00"
---
Mozilla は今週、[Firefox 47 Beta と 48 Developer Edition](https://www.mozilla.org/firefox/channel/) を公開しました。私たちがバージョンごとにまとめている [サイト互換性ドキュメント](https://www.fxsitecompat.dev/ja/docs/) に目を通してください。

* [Firefox 47 サイト互換性情報](https://www.fxsitecompat.dev/ja/versions/47/)
* [Firefox 48 サイト互換性情報](https://www.fxsitecompat.dev/ja/versions/48/)

今週火曜日に公開された Firefox 46 のリグレッションを見つけるためいくつかの情報源を監視していますが、幸い今のところ重大な問題は見つかっていません。ただし、以下のような WebGL のリグレッションと `<input>` バリデーションエラーが発見されています。

* [WebGL のポイントスプライトが特定の環境で正しく描画されません](https://www.fxsitecompat.dev/ja/docs/2016/webgl-point-sprites-are-not-rendered-properly-in-certain-environments/)
* [`<input pattern>` が正規表現に `u` フラグを設定するようになりました](https://www.fxsitecompat.dev/ja/docs/2016/input-pattern-now-sets-u-flag-for-regular-expressions/)

他に何か変更点やリグレッションに気付いた場合は [ご一報ください](https://www.fxsitecompat.dev/ja/contribute/)！

**更新**: 現在 Firefox 46 に見つかった以下のバグをトラッキングしています。

* [Bug 1269170 - KanColle, a popular Flash game doesn't work with Firefox 46, raising a connection error](https://bugzilla.mozilla.org/show_bug.cgi?id=1269170)
* [Bug 1269184 - The menu on ADS-B Exchange Global Radar View is not visible on Firefox 46 and 47](https://bugzilla.mozilla.org/show_bug.cgi?id=1269184)
