---
title: "`Function.length` がデフォルト引数を数えなくなりました"
date: "2013-01-03T03:53:26-05:00"
categories: ["javascript"]
tags: []
versions: ["18"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=777061"
      title: "Bug 777061 – Function .length property should not count rest parameters or parameters with default values"
---
関数が期待する引数の数を示す [`Function.length`](https://developer.mozilla.org/docs/JavaScript/Reference/Global_Objects/Function/length) プロパティは、従来 [デフォルト値付き引数](https://developer.mozilla.org/docs/JavaScript/Reference/default_parameters) を含んでいました。そうした引数を含まないように修正が行われました。そのため `(function (a, b, c = false) {}).length` は `3` ではなく `2` となります。
