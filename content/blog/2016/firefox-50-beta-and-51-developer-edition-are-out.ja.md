---
title: "Firefox 50 Beta と 51 Developer Edition が公開されました"
date: "2016-09-24T19:33:00-04:00"
---
Mozilla は今週、Firefox 49、[Firefox 50 Beta と 51 Developer Edition](https://www.mozilla.org/firefox/channel/) を公開しました。私たちがバージョンごとにまとめている [サイト互換性ドキュメント](https://www.fxsitecompat.com/ja/docs/) に目を通してください。

* [Firefox 49 サイト互換性情報](https://www.fxsitecompat.com/ja/versions/49/)
* [Firefox 50 サイト互換性情報](https://www.fxsitecompat.com/ja/versions/50/)
* [Firefox 51 サイト互換性情報](https://www.fxsitecompat.com/ja/versions/51/)

Firefox 49 における注目すべき変更点のひとつは [`#RGBA` カラー値対応](https://www.fxsitecompat.com/ja/docs/2016/support-for-rgba-colour-values-may-validate-previously-invalid-values/) で、これはある Microsoft 製アプリケーションとおそらく他のサイトにも影響しています。テキストが透明に表示されてしまうのを防ぐため、あなたのスタイルシートも調べた方がいいでしょう。

Firefox 50 Beta では、まだ様々なサイトで見られる [安全でないログインフォームの警告](https://www.fxsitecompat.com/ja/docs/2015/non-https-sites-containing-login-form-will-be-marked-insecure/) が有効となりました。訪問者を守るため、今こそあなたのサイト全体を暗号化する時です。

なお、現在 Nightly チャンネルで公開されている Firefox 52 でいよいよ [Flash を除くプラグイン対応が廃止される](https://www.fxsitecompat.com/ja/docs/2015/plug-in-support-will-be-dropped-by-the-end-of-2016-except-flash/) ことを忘れないでください。もしあなたのサイトに Silverlight や Java といったプラグインに依存するコンテンツがある場合は、早急にそれを置き換える計画を立てるべきです。
