---
title: "テーブル要素上の `position:relative` が無視されなくなります"
date: "2014-03-21T04:50:04-04:00"
categories: ["css"]
tags: []
versions: ["30"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=63895": "Bug 63895 – positioned internal table elements not abs pos containing block"
---
従来、テーブル要素上で指定された `position:relative` は、CSS2 仕様の中ではその効果が「未定義」とされていたため、Firefox 上では無視される一方、他のブラウザでは「期待通りに」動作していました。テーブルセル内に絶対配置要素を含めたい場合、[`<td>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/td) 直下に相対配置の [`<div>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/div) 要素を追加することが一般的な回避策として行われていました。

CSS3 仕様の中でその効果が定義されたため、`position:relative` を受け入れるよう Firefox の実装が変更されました。なお、後方互換のため、上記の回避策は Firefox 24 [<abbr title="Extended Support Release">ESR</abbr>](http://www.mozilla.jp/business/downloads/) が 2014 年 10 月中にサポート終了となるまで残しておいた方が良いでしょう。

この変更には、[`<td>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/td) 以外のテーブル要素に `position:relative` を適用しつつ、何も効果がないことを作者が期待しているページのレイアウトを崩す潜在的な可能性があります。そうした場合、[Web コンソール](https://developer.mozilla.org/ja/docs/Tools/Web_Console) は問題の特定を容易にするため警告を表示します。
