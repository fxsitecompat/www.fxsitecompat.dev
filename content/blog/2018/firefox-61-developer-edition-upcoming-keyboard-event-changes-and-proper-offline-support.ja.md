---
title: "Firefox 61 Developer Edition、近く予定されているキーボードイベント関連の変更、正しいオフライン対応"
date: "2018-05-09T21:37:00-04:00"
aliases:
    - "/ja/blog/2018/firefox-61-developer-edition-upcoming-keyboard-event-changes-and/"
---
Mozilla は [Firefox 61 Beta と Developer Edition](https://www.mozilla.org/firefox/channel/desktop/) を公開しました。6 月下旬公開の最終版に備えて [Firefox 61 互換性情報](https://www.fxsitecompat.dev/ja/releases/61/) を確認してください。

ブラウザーのキーボードイベント処理に関して近々予定されている変更が 2 件あります。[1 つ目](https://www.fxsitecompat.dev/ja/docs/2018/keydown-and-keyup-events-will-soon-be-fired-during-ime-composition/) は東アジアのユーザーに対応しているアプリケーションに影響する潜在的な可能性を持ったものですが、[2 つ目](https://www.fxsitecompat.dev/ja/docs/2018/non-printable-keys-will-soon-stop-firing-keypress-event/) については *Google Docs* など人気アプリケーションも正常に動作しなくなることが判明しています。ウェブ開発者の皆さんには、これらを確認して、[プレリリース版](https://www.mozilla.org/firefox/channel/desktop/) のいずれかで新たな挙動をテストするよう強く推奨します。

[もうひとつ注目すべき変更](https://www.fxsitecompat.dev/ja/docs/2018/online-offline-events-are-no-longer-fired-on-document-and-document-body/) は `online`、`offline` イベントに関するもので、これらは今後 `document` 上で発生しなくなります。MDN 上の関連記事を含め、一部のコードサンプルやドキュメントが従来の間違った実装を元に書かれていることから、オフライン対応を備えたウェブアプリの中にはこの変更の影響を受けるものがあるかもしれません。幸い解決策は非常に単純で、`document` を `window` に置き換えるだけです。
