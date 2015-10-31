---
title: "`window.sidebar` が削除されます"
date: "2015-10-25T22:07:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=862147": "Bug 862147 - drop support for window.sidebar"
---
廃止予定となっている非標準の [`window.sidebar`](https://developer.mozilla.org/ja/docs/Web/API/window.sidebar) オブジェクトが近い将来削除されることとなりました。`addPanel` メソッドは [Firefox 23 で削除され](https://www.fxsitecompat.com/ja/docs/2013/ability-to-add-a-sidebar-panel-has-been-dropped/)、`addSearchEngine` メソッドは [Firefox 44 で Sherlock 対応を中止](https://www.fxsitecompat.com/ja/docs/2015/sherlock-search-plug-ins-are-no-longer-supported/) しており、このオブジェクトはもはや役に立ちません。ただ、まだ一部のサイトでブラウザ判別に使用されているようです。Web 開発者はこれを使うのをやめてください。
