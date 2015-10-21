---
title: "`HTMLInputElement.inputmode` が初期設定で無効化されました"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
versions: ["21"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=857355": "Bug 857355 – Hide HTMLInputElement\'s inputMode API behind a pref and only turn it on for Aurora/Nightly"
---
Firefox 17 以降 [実装](https://bugzilla.mozilla.org/show_bug.cgi?id=746142) されている [`HTMLInputElement`](https://developer.mozilla.org/ja/docs/Web/API/HTMLInputElement) の `inputmode` API が、仕様がまだ安定していないという理由から、初期設定で無効化されました。この機能を試すには、設定 `dom.forms.inputmode` を有効化するか、[Aurora](http://www.mozilla.org/en-US/firefox/aurora/) チャンネルを使う必要があります。なお、この API は [Firefox 22 で `inputMode` (大文字の `M`) に改名されます](https://www.fxsitecompat.com/ja/docs/2013/htmlmediaelement-crossorigin-and-htmlinputelement-inputmode-have-been-renamed/)。
