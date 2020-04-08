---
title: "Firefox 76 Beta と Developer Edition が公開、COVID-19 の発生により一部の変更は延期に"
date: "2020-04-07T22:28:00-04:00"
---
Mozilla は今日、[サイト互換性に関する変更を少しだけ含んだ](https://www.fxsitecompat.dev/ja/versions/76/) [Firefox 76 Beta と Developer Edition](https://www.mozilla.org/firefox/channel/desktop/) を公開しました。

既にご存知かもしれませんが、COVID-19 の世界的大流行は、目下 Firefox や他のブラウザーの開発に多少なりとも影響を及ぼしています。この異例の期間中、世界中で膨大な数の人々が自宅での勤務や勉強を続けており、[Firefox を含む](https://blog.mozilla.org/data/2020/03/30/opening-data-to-understand-social-distancing/) デスクトップブラウザーを使い、様々なオンラインリソースに依存しています。

Mozilla は高速リリーススケジュールを維持していますが、サイトに不具合をもたらす可能性を最小限に抑えるため、後方互換性のない変更をいくつか延期しています。

* [TLS 1.0/1.1 対応の廃止](https://www.fxsitecompat.dev/ja/docs/2020/tls-1-0-1-1-support-has-been-removed/)
* [WebRTC の DTLS 1.0 対応の廃止](https://www.fxsitecompat.dev/ja/docs/2020/dtls-1-0-support-in-webrtc-has-been-removed/)
* FTP 対応の廃止 (まもなく Firefox Nightly では実施)
* [ワーカースクリプトの MIME 判別強制](https://www.fxsitecompat.dev/ja/docs/2020/worker-scripts-with-wrong-mime-type-will-be-blocked-from-loading-with-worker-or-sharedworker/)
* [JPEG 画像の回転](https://www.fxsitecompat.dev/ja/docs/2020/jpeg-images-are-now-rotated-by-default-according-to-exif-data/)

これらの変更は状況が改善してから今年後半に行われる予定です。今後も当サイトでは最新情報をお伝えします。
