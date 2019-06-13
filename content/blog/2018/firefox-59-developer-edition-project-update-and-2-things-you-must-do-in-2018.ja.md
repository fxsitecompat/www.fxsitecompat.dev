---
title: "Firefox 59 Developer Edition、プロジェクト最新情報、あなたが 2018 年にすべき 2 つのこと"
date: "2018-01-25T12:34:00-05:00"
---
Mozilla は先週 [Firefox 59 Beta と Developer Edition](https://www.mozilla.org/firefox/channel/desktop/) を公開しました。3 月公開の最終版に備えて [Firefox 59 互換性情報](https://www.fxsitecompat.dev/ja/versions/59/) を確認してください。Firefox 58 と同様に、さらに多くの非標準機能が削除される予定です。

これが 2018 年最初のブログ記事となるので、私たちやあなたが今年すべきことを簡単にまとめておきたいと思います。

## 私たちの 2018 年の計画

まず、私たちからは良いニュースがあります！ Mozilla がこのイニシアチブの「実質的な」スポンサーとなりました。プロジェクトマネージャーである [Kohei Yoshino](https://github.com/kyoshino) がインディペンデントコントラクターとして [Release Management チーム](https://release.mozilla.org/) のために働いている間、組織内部の人たちとより密接に協力できる機会を得られることに興奮しています。

この小さなプロジェクトは 2012 年以来活動を続けています。それは、私たちのドキュメント、ツイート、リグレッション調査が、Mozilla とウェブ開発者の関係や Firefox の製品品質を向上させるのに役立つと信じているからです。今回、Mozilla がこのたゆみない努力に燃料を注いでくれることになりました。これは言うまでもなく、お互いの利益になる状況です :-)

実のところ私たちはまだ今年の計画を練っているところですが、皆さんのためになるよう、先延ばしになっているサイトのリデザインに優先的に取り組みます。

## あなたの 2018 年の計画

### HTTPS へのサイト移行

Mozilla は先週、すべての新機能や一部既存機能について [HTTPS を必須とする](https://blog.mozilla.org/security/2018/01/15/secure-contexts-everywhere/) 方針を発表しました。Geolocation API の使用は既に [Firefox 55](https://www.fxsitecompat.dev/ja/docs/2017/use-of-geolocation-api-is-now-limited-to-secure-sites/) 以降安全なサイトに制限されています。次の予定は Application Cache と [WebVR](https://www.fxsitecompat.dev/ja/docs/2017/webvr-can-no-longer-be-used-on-insecure-sites/) で、それに Notifications、Web Crypto、Encrypted Media Extensions の各 API が続く可能性があります。

もしあなたがこれらの機能のいずれも使用していない場合でも、HTTPS への移行はもはや任意とは見なされません。Mozilla などが資金を提供している [Let's encrypt](https://letsencrypt.org/) は、移行をさらに容易にするため、2 月下旬から [無料ワイルドカード証明書](https://letsencrypt.org/2017/07/06/wildcard-certificates-coming-jan-2018.html) の提供を開始します。

### Flash 依存の廃止

もしかしてまだ Flash に頼っていますか？ 残念ながら、Flash プラグイン対応は 2020 年末までに Firefox や他のブラウザーから [削除される予定です](https://blog.mozilla.org/futurereleases/2017/07/25/firefox-roadmap-flash-end-life/)。最新の [Firefox Hardware Report](https://hardware.metrics.mozilla.com/) によれば、既に現時点でも Firefox ユーザーの 3 分の 1 以上はもはや Flash Player を使用していません。あなたのサイト上で最大限のアクセシビリティを確保するため、できるだけ早くすべての Flash コンテンツを標準技術に置き換えるべきです。
