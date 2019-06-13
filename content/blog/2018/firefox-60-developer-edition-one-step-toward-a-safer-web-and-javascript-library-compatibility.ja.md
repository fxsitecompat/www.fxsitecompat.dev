---
title: "Firefox 60 Developer Edition、より安全なウェブへ向けた一歩、JavaScript ライブラリの互換性"
date: "2018-03-19T20:13:00-04:00"
---
Mozilla は [Firefox 60 Beta と Developer Edition](https://www.mozilla.org/firefox/channel/desktop/) を公開しました。5 月上旬公開の最終版に備えて [Firefox 60 互換性情報](https://www.fxsitecompat.dev/ja/versions/60/) を確認してください。

見ての通り、安全なコンテキストの必須化や [Symantec 証明書無効化措置の第 1 弾](https://www.fxsitecompat.dev/ja/docs/2018/symantec-certificates-issued-before-june-2016-are-now-distrusted/) など、いくつかのセキュリティ関連の変更があります。GeoTrust、RapidSSL、Symantec、Thawte あるいは Verisign ブランドの付いた SSL/TLS サーバー証明書を使っている場合、あなたのサイト上で「安全でない接続」エラーページを避けるため、直ちに行動を起こしてください。まだ何も証明書を持っていないなら、[Let's Encrypt](https://letsencrypt.org/) から無料で手に入れましょう。

[Firefox 60 で再度有効化される](https://www.fxsitecompat.dev/ja/docs/2018/array-prototype-values-is-now-enabled-again/) ことになった `Array.prototype.values()` は、新機能の追加がどのように [既存のウェブアプリを壊す](https://www.fxsitecompat.dev/ja/docs/2016/array-prototype-values-breaks-some-legacy-apps/) 可能性があるかという一例でしたが、これは新しい問題ではなく、また最後でもありません。[Firefox 25 で追加された](https://www.fxsitecompat.dev/ja/docs/2013/es6-array-methods-have-been-added/) `Array.prototype.find()` は Sugar ライブラリを使っているサイトを壊しました。一方、現在実装が行われている `Array.prototype.flatten()` は [MooTools に影響する](https://bugzilla.mozilla.org/show_bug.cgi?id=1443630) ことが分かっており、これは実のところ `String.prototype.contains()` でも [同じ問題](https://www.fxsitecompat.dev/ja/docs/2012/mootools-1-2-x-is-not-compatible-with-firefox-18-and-newer/) を抱えていました。お使いの JavaScript ライブラリを最新に保つことを忘れずに！
