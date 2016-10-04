---
title: "`Array.prototype.values()` が一部の古いアプリに影響しています"
date: "2016-09-21T21:07:00-04:00"
categories: ["javascript"]
tags: []
versions: ["48"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1299593"
      title: "Bug 1299593 - Microsoft Dynamics CRM 2011 Lookup Error since Firefox Version 48.0.2 due to Array.prototype.values"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1299444"
      title: "Bug 1299444 - Blank calendar section in MS Outlook webmail (OWA) after Firefox 48"
---
Firefox 48 で ECMAScript 2015 (ES6) の [`Array.prototype.values`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/values) メソッドへの対応が追加されました。Microsoft Edge や Apple Safari にも実装されているこの新メソッドが原因で、*Microsoft Dynamics CRM 2011* や *Outlook Web App* といったアプリケーションが正常に動作していないとの報告がいくつかあります。Mozilla 開発者は Firefox でこのメソッドを無効化することを検討しています。

**更新**: 互換性問題を防ぐため `values` メソッドは Firefox 50 で無効化されました。ただし Firefox Nightly では引き続き使用可能です。
