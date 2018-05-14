---
date: "2018-05-13T17:24:00-04:00"
title: "開発者向けツール"
description: "私たちは、開発者の仕事を楽にするような、いくつかのツールを作成しています。"
slug: "tools"
---
## 互換性データセット

私たちがまとめてきた [700 ページ以上の記事](https://www.fxsitecompat.com/ja/docs/) を元に、Nightly、Beta/DevEdition、ESR を含む各 Firefox チャンネル上での時代遅れとなった機能の状況をカバーする、最新の正確なサイト互換性データセットを公開します。データは 2018 年の第 3 四半期までに可搬性の高い JSON 形式で提供される予定です。

言うまでもなく、私たちは *MDN* や *Can I use*、*QuirksMode* で見られるような包括的なブラウザー対応テーブルを作ろうとしているのではありませんが、チャンネルごとの廃止予定の詳細を含めることで、私たち独自のデータセットは Firefox 開発者とウェブ開発者の双方にとって役立つものとなるだろうと期待しています。

## 互換性チェッカー

基礎データが整ったところで、[Firefox 開発ツール](https://developer.mozilla.org/docs/Tools) 向け拡張機能の提供も行います。現在開かれているページ上で削除あるいは廃止予定となった機能が使われていた場合にその一覧が表示され、ウェブ開発は即座に修正することが可能となります。技術的制約から、今後公開されるデータセットに含まれるすべての機能をチェックすることは困難ですが、[HTML](https://www.fxsitecompat.com/ja/categories/html/)、[CSS](https://www.fxsitecompat.com/ja/categories/css/)、[JavaScript](https://www.fxsitecompat.com/ja/categories/javascript/)、[DOM](https://www.fxsitecompat.com/ja/categories/dom/) 内のほとんどの問題は列挙できるでしょう。

このチェッカーは、未対応の機能や他のブラウザーも扱うために外部の互換性データを一部活用する可能性があります。また、リグレッションアラートやレポーターといったいくつかのユーティリティによって利便性を向上させることも検討しています。
