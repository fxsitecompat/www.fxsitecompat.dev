---
title: "`RegExp` の `global`、`ignoreCase`、`multiline`、`sticky` プロパティがプロトタイプアクセサプロパティになりました"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
versions: "38"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1120169": "Bug 1120169 - Implement RegExp.prototype.{global, ignoreCase, multiline, source, sticky, unicode}"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1138325": "Bug 1138325 - Turning RegExp#source from an instance property into an accessor breaks ClojureScript apps"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1150297": "Bug 1150297 - Move source property to RegExp instance again."
---
[`RegExp`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/RegExp) インスタンスプロパティの [`global`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Regexp/global)、[`ignoreCase`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Regexp/ignoreCase)、[`multiline`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Regexp/multiline)、[`sticky`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Regexp/sticky) がプロトタイプアクセサへ移され、[`RegExp.prototype.global`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Regexp/global)、[`RegExp.prototype.ignoreCase`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Regexp/ignoreCase)、[`RegExp.prototype.multiline`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Regexp/multiline)、[`RegExp.prototype.sticky`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Regexp/sticky) となりました。[`source`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Regexp/source) プロパティへの変更は Web 互換性の問題により [Firefox 40](http://www.fxsitecompat.com/ja/versions/40/) へ延期されました。
