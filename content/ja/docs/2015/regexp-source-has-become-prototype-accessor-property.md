---
title: "`RegExp.source` がプロトタイプアクセサプロパティとなりました"
date: "2015-06-13T15:20:46-04:00"
categories: ["javascript"]
tags: []
versions: "41"
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1120169": "Bug 1120169 - Implement RegExp.prototype.{global, ignoreCase, multiline, source, sticky, unicode}"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1138325": "Bug 1138325 - Turning RegExp#source from an instance property into an accessor breaks ClojureScript apps"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1150297": "Bug 1150297 - Move source property to RegExp instance again."
---
[`RegExp`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/RegExp) インスタンス上の `source` プロパティがプロトタイプアクセサへ移され、[`RegExp.prototype.source`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/RegExp/source) プロパティとなりました。この変更は元々 [他のプロパティとともに](https://www.fxsitecompat.com/ja/docs/2015/regexp-global-ignorecase-multiline-and-sticky-properties-are-now-prototype-accessor-properties/) Firefox 38 で行われましたが、Web 互換性問題のためバックアウトされていました。あなたのアプリで [*ClojureScript*](https://github.com/clojure/clojurescript) が使われている場合、そのライブラリを最新版へ更新しないと Firefox 41 以降のバージョンで動かなくなる可能性があります。
