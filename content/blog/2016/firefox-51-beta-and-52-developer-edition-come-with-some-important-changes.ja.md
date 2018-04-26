---
title: "Firefox 51 Beta と 52 Developer Edition でいくつかの重要な変更が予定されています"
date: "2016-12-04T15:30:00-05:00"
---
Mozilla は [Firefox 51 Beta と 52 Developer Edition](https://www.mozilla.org/firefox/channel/desktop/) をそれぞれ 11 月 16 日と 21 日にリリースしました。このブログ記事はもっと早く投稿すべきでした。今週行われる Mozilla All Hands (当プロジェクトのマネージャー [Kohei](https://mozillians.org/u/kohei.yoshino/) はボランティアとして参加します) やそれに続くホリデーシーズンのため、[Firefox 51 は 1 月下旬まで公開されません](https://release.mozilla.org/firefox/50/2016/11/22/Firefox50-planned-dot-release.html)。それはともかく、各バージョンのサイト互換性情報を見てみてください。

* [Firefox 51 サイト互換性情報](https://www.fxsitecompat.com/ja/versions/51/)
* [Firefox 52 サイト互換性情報](https://www.fxsitecompat.com/ja/versions/52/)

以下にいくつか重要なポイントをまとめました。

* Firefox 51 の時点で、[公開認証局から発行された SHA-1 証明書は受け入れられなくなります](https://www.fxsitecompat.com/ja/docs/2016/sha-1-certificates-issued-by-public-ca-will-no-longer-be-accepted/)。Mozilla によれば、現在の SHA-1 使用率は 1% 以下ですがゼロではないため、Developer Edition を使ってあなたの安全なサイトがブロックされていないことを再確認するのは良い考えと言えるでしょう。
* Firefox 51 では [安全でないパスワード入力警告も初期設定で有効となります](https://www.fxsitecompat.com/ja/docs/2016/insecure-password-input-warning-will-be-enabled-by-default/)。互換性の観点からは特に何か動作しなくなるということはありませんが、あなたはおそらくサイトに来たお客さんに壊れた南京錠アイコンを見せたなくないでしょうから、ログインフォームは速やかに HTTPS ページへ移動しましょう。
* Firefox 52 では [Windows デスクトップ上でのタッチイベント対応が有効化されます](https://www.fxsitecompat.com/ja/docs/2016/touch-event-support-has-been-re-enabled-on-windows-desktop/)。ドキュメントで説明している通り、モバイル判別にタッチイベントを頼ってはいけません。さもないと、あなたのサイトはタッチパネル搭載のノートパソコンを使っている人たちにとって使いものにならなくなります。
* 最後に最も重要な変更ですが、Firefox 52 でとうとう [Flash 以外のプラグイン対応が廃止されます](https://www.fxsitecompat.com/ja/docs/2016/plug-in-support-has-been-dropped-other-than-flash/)。つまり、Java アプレットや Silverlight 動画は今後動作しなくなります。あなたが影響を受ける場合は、Firefox 52 が 3 月上旬に一般公開される前に迅速な対応を取ってください。

2016 年もほぼ終わりということで、私たちはプロジェクトをアップグレードすべく 2017 年に向けた計画を立てようとしています。もっとたくさんのツイート？ サイトの改良？ あなたが必要とするものを聞かせてください。また、今は年末の資金調達シーズンでもあるので、私たちはあなたから [少額の寄付](https://www.fxsitecompat.com/ja/contribute/#%E5%AF%84%E4%BB%98) をもらえれば大変嬉しく思います。言うまでもなく所得税控除の対象とはなりませんが、たとえ数ドルでも十分です。あなたの支援に感謝します！
