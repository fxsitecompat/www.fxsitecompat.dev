---
title: "Firefox 77 Beta と Developer Edition 公開、COVID-19 が引き続き開発に影響"
date: "2020-05-05T22:59:00-04:00"
---
Mozilla は今日 [Firefox 77 Beta と Developer Edition](https://www.mozilla.org/firefox/channel/desktop/) を公開しました。

COVID-19 の世界的流行により世界中でまだ多くの企業や個人が大きな課題に直面していることから、Firefox 開発者は [JPEG 画像の自動回転](https://www.fxsitecompat.dev/ja/docs/2020/jpeg-images-are-now-rotated-by-default-according-to-exif-data/) を除いて後方非互換な変更を含めることを避けました。これは少なくとも *Slack* に不具合をもたらすことが判明しているものの、Google も既に同じ改良を含んだ Chrome を提供しているため同じ問題が見られます。実際のところ、本稿執筆時点で `image-orientation` CSS プロパティへの変更はまだ Firefox 77 へ投入されていませんが、おそらく来週にはベータ版に入るものと思います。

[Application Cache ストレージの廃止](https://www.fxsitecompat.dev/ja/docs/2020/application-cache-storage-has-been-removed/) は当初 Firefox 77 で予定されていましたが、延期されました。

Firefox 77 に関しては以上です。

今後のリリースについて言えば、Firefox 78 は次期法人向け [延長サポート版](https://support.mozilla.org/kb/choosing-firefox-update-channel) (ESR) となるため、互換性に影響を与える変更は再び避けられます。今後数週間のうちに、私たちは COVID-19 のために延期されているすべての変更を文書化していきます。それらは Firefox 79 あるいはそれ以降で投入されることとなります。

私たちはまた、[Firefox 開発ツール拡張機能](https://addons.mozilla.org/firefox/addon/site-compatibility-tools/) に含まれている互換性チェッカーにも鋭意取り組んでいます。近く CSS 対応も入りますのでお楽しみに。
