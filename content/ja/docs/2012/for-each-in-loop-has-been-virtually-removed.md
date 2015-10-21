---
title: "`for each...in` ループが実質的に削除されました"
date: "2012-12-29T08:29:30-05:00"
categories: ["javascript"]
tags: []
versions: ["20"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=804834": "Bug 804834 – Hide \"for each\" from content"
---
[E4X](https://developer.mozilla.org/ja/docs/E4X) は [Firefox 17 で廃止予定となり無効化されました](https://www.fxsitecompat.com/ja/docs/2012/e4x-has-been-disabled/) が、その一部として標準化された [`for each...in`](https://developer.mozilla.org/ja/docs/JavaScript/Reference/Statements/for_each...in) 文は後方互換性のため残されています。Firefox 20 では、`<script type="text/javascript;version=1.6">` のように Web 開発者が JavaScript 1.6 以降を明示的に指定した場合を除いて使用できなくする変更が行われました。今後は [ECMAScript 6](https://developer.mozilla.org/ja/docs/JavaScript/ECMAScript_6_support_in_Mozilla) で標準化が進められている [`for...of`](https://developer.mozilla.org/ja/docs/JavaScript/Reference/Statements/for...of) 文による代用が推奨されます。
