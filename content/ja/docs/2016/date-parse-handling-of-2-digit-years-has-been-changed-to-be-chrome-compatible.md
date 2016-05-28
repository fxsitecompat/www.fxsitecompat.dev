---
title: "`Date.parse` による 2 桁年の扱いが Chrome 互換に変更されました"
date: "2016-05-28T02:47:00-04:00"
categories: ["javascript"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1265136"
      title: "Bug 1265136 - new Date(<mm/dd/yy>) behaves differently in Firefox vs Chrome/Safari"
---
[`Date`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) コンストラクタや [`Date.parse`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/parse) メソッドによる文字列解析は実装依存であり、Firefox は 2 桁年を Internet Explorer と同じ方法で扱ってきました。Firefox 49 で [このロジックが変更されて](https://hg.mozilla.org/mozilla-central/rev/138521110469) Google Chrome 互換となり、`50` 以下の 2 桁年はすべて 21 世紀の年として扱われるようになりました。例えば、従来 1917 年 4 月 16 日として解析されていた `04/16/17` は 2017 年 4 月 16 日となります。相互運用性の観点から、Web 開発者には常に `2017-04-16` のような ISO 8601 形式を使うよう推奨します。
