---
title: "`XMLDocument.load()` と `XMLDocument.async` が廃止されました"
date: "2019-05-28T01:20:00-04:00"
categories: ["dom"]
tags: []
versions: ["68"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=332175"
      title: "Bug 332175 - Drop XMLDocument.load() support"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1328138"
      title: "Bug 1328138 - Remove XMLDocument's async IDL attribute"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1546112"
      title: "Bug 1546112 - Remove the code for XMLDocument.load/async if possible"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1569102"
      title: "Bug 1569102 - xmldocument load type error"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/0T4l3yaP3g4/discussion"
      title: "Intent to unship: XMLDocument.load and XMLDocument.async APIs"
---
Firefox 68 で `XMLDocument` インターフェイスから [`load`](https://developer.mozilla.org/docs/Web/API/XMLDocument/load) メソッドと [`async`](https://developer.mozilla.org/docs/Web/API/XMLDocument/async) プロパティへの対応が削除されました。これは、リモートの XML ドキュメントを同期的または非同期的に取得するために使用できた非常に古い非標準の API でしたが、後に `XMLHttpRequest` に取って代わられました。標準化されたことも、Firefox 以外のブラウザーに実装されたこともありません。しかし、Mozilla は未だにこの API が若干ながら使用されていることを確認しているため (0.01% 以下)、ウェブ開発者の皆さんには、古いコードを検索し、代わりに `XMLHttpRequest` か `fetch()` を使うよう推奨します。

**更新**: 古いアプリケーションとの互換性を保つため、この変更は Firefox 68 ESR ([68.1.0](https://www.mozilla.org/en-US/firefox/68.1.0/releasenotes/) 以降) では取り消されました。関連コードは Firefox 71 で完全に削除されたため、いずれにしてもこの古い機能を使っているアプリケーションは 2020 年 6 月公開の Firefox 78 ESR に向けて更新が必要です。
