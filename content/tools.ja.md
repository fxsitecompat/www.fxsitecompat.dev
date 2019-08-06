---
date: "2018-05-13T17:24:00-04:00"
title: "開発者向けツール"
description: "私たちは、開発者の仕事を楽にするような、いくつかのツールを作成しています。"
slug: "tools"
---
## 互換性データセット

私たちがまとめてきた [800 ページ以上の記事](https://www.fxsitecompat.dev/ja/docs/) を元に、Nightly、Beta/DevEdition、ESR を含む各 Firefox チャンネル上での時代遅れとなった機能の状況をカバーする、最新の正確なサイト互換性データセットを公開します。データは可搬性の高い JSON 形式で提供される予定です。

言うまでもなく、私たちは *MDN* や *Can I use*、*QuirksMode* で見られるような包括的なブラウザー対応テーブルを作ろうとしているのではありませんが、チャンネルごとの廃止予定の詳細を含めることで、私たち独自のデータセットは Firefox 開発者とウェブ開発者の双方にとって役立つものとなるだろうと期待しています。

## Firefox 拡張機能

私たちは Firefox の開発者ツール内で直接サイト互換性問題を把握、確認、報告できる便利なオールインワンツールとして [Firefox 向け拡張機能](https://addons.mozilla.org/firefox/addon/site-compatibility-tools/) を開発しています。初回リリースではドキュメントへのアクセスや互換性問題の報告を簡単にしました。

基礎データセットが整ったところで、この拡張機能に互換性チェッカーを統合する予定です。現在開かれているページ上で削除あるいは廃止予定となった機能が使われていた場合にその一覧が表示され、ウェブ開発は即座に修正することが可能となります。技術的制約から、今後公開されるデータセットに含まれるすべての機能をチェックすることは困難ですが、[HTML](https://www.fxsitecompat.dev/ja/categories/html/)、[CSS](https://www.fxsitecompat.dev/ja/categories/css/)、[SVG](https://www.fxsitecompat.dev/ja/categories/svg/)、[JavaScript](https://www.fxsitecompat.dev/ja/categories/javascript/)、[DOM](https://www.fxsitecompat.dev/ja/categories/dom/) 内のほとんどの問題は列挙できるでしょう。

<img src="/images/screenshots/firefox-extension-large.png" alt="" width="800" height="450">

## VS Code 拡張機能

私たちは Visual Studio Code 向けの拡張機能を公開する計画も立てています。
