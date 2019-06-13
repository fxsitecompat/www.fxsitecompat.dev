---
title: "2 件の互換性問題を伴った Firefox 62 が 3 週間後に公開されます"
date: "2018-08-15T15:09:00-04:00"
---
しばらくの間他のことで忙しかったため、次回リリースに向けたブログ記事の投稿が遅くなってしまいました。申し訳ありません。

Firefox 62 は現在までに 8 週間 Beta/DevEdition チャンネル上で配信されていて、3 週間後の 9 月 5 日に正式公開となります。皆さん既に [Firefox 62 サイト互換性情報](https://www.fxsitecompat.dev/ja/versions/62/) に目を通されているかもしれませんが、ここでいくつかアップデートがあります。

* [`URL.createObjectURL()` が `MediaStream` を引数として受け付けなくなりました](https://www.fxsitecompat.dev/ja/docs/2018/url-createobjecturl-no-longer-accepts-mediastream-as-argument/): この変更により *Facebook Live* が使えなくなることが判明しています。もしあなたが似たようなライブストリーミングサービスを提供しているなら、引き続き支障なく動作することを確認してください。
* [`Event.prototype.srcElement` への対応が追加されました](https://www.fxsitecompat.dev/ja/docs/2018/support-for-event-prototype-srcelement-has-been-added/): この IE 由来のプロパティはウェブ互換性のために実装され、中国のポータルサイト *QQ.com* が影響を受けています。Firefox 63 にも知っておくべき [別のプロパティ追加](https://www.fxsitecompat.dev/ja/docs/2018/window-event-has-been-added-for-compatibility-but-some-browser-detections-are-broken/) があります。
* [`getComputedStyle()` がスタイルを取得できない場合に `null` を返さないようになりました](https://www.fxsitecompat.dev/ja/docs/2018/getcomputedstyle-no-longer-returns-null-when-style-can-t-be-retrieved/): この記事は昨日投稿されました。もしまだ見てないなら確認してください。

私たちは [Firefox 63 サイト互換性情報](https://www.fxsitecompat.dev/ja/versions/63/) の準備にも着手しています。重要な変更のひとつは [Symantec、GeoTrust、RapidSSL、Thawte、Verisign 証明書への信頼取り消し](https://www.fxsitecompat.dev/ja/docs/2018/symantec-geotrust-rapidssl-thawte-verisign-certificates-will-all-be-distrusted-in-october-2018/) で、これは *PayPal* や *Etsy* といった一部のメジャーサイトにも影響することが判明しています。予期せぬサービス中断を防ぐため、サイトの SSL/TLS 証明書を再確認しましょう。
