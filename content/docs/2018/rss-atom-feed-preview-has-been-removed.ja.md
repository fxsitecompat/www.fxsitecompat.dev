---
title: "RSS/Atom フィードプレビューが廃止されました"
date: "2018-10-23T01:07:00-04:00"
categories: ["misc"]
tags: []
releases: ["64", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1477667"
      title: "Bug 1477667 - [meta] Remove feed reader and live bookmarks support from Firefox"
---
RSS/Atom フィードプレビューと組み込みの [ライブブックマーク](https://support.mozilla.org/kb/live-bookmarks) フィードリーダー機能が、低普及率を原因として、Firefox 64 で廃止されました。今後、サーバーの設定に応じて、ウェブフィードは通常の XML ファイルとして表示あるいはダウンロードされます。

より良いユーザー体験のため、ウェブマスターの皆さんは、フィードへの直リンクを [Feedly](https://feedly.com/factory.html) など外部サービスの購読リンクに置き換えるか、少なくともフィードがダウンロードされないよう確認した方が良いかもしれません。ちなみに、RSS と Atom フィードの適切な MIME タイプはそれぞれ `application/rss+xml` と `application/atom+xml` です。

一般的なフィードリーダーは `<link rel="alternate">` でフィードを発見すると思われるので、それはそのまま維持すべきです。
