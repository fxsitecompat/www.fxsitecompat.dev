---
title: "印刷用スタイルシートの `page-break-before`/`after` が要素の欠落や重複につながる場合があります"
date: "2017-11-10T03:43:00-05:00"
categories: ["css"]
tags: []
versions: ["56"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1308876"
      title: "Bug 1308876 - Nested inline-blocks with matching width locks up browser due to O(2^depth) reflow performance"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1406291"
      title: "Bug 1406291 - floating table following quickly after page-break-after style is not printed"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1404868"
      title: "Bug 1406356 - overlapping content following page-break-before in Firefox 56"
---
あるパフォーマンス改善が原因で印刷に関するリグレッションが Firefox 56 で発生しました。この原因は実のところ、別記事で解説している [マルチカラムレイアウトのリグレッション](https://www.fxsitecompat.dev/ja/docs/2017/certain-multi-column-layouts-may-balance-unevenly-or-lack-elements-randomly/) の原因と同じです。

印刷用スタイルシートで要素に [`page-break-before`](https://developer.mozilla.org/docs/Web/CSS/page-break-before) あるいは [`page-break-after`](https://developer.mozilla.org/docs/Web/CSS/page-break-after) プロパティが指定されていると、それに続く要素が消えたり、前の要素と重なり合ったりする場合があります。これらの問題はドキュメントの印刷出力のみに影響し、ブラウザー内でのページの描画は問題ありません。Mozilla 開発者がじきに問題を調査します。
