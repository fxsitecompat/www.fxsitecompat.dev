---
title: "`Array.values()` が再度有効化されました"
date: "2018-02-11T00:08:00-05:00"
categories: ["javascript"]
tags: []
releases: ["60", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1420101"
      title: "Bug 1420101 - Array.prototype.values() does not exist"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/s92kdFNjL0U/discussion"
      title: "Intent to ship: Array.prototype.values"
aliases:
    - "/ja/docs/2018/array-prototype-values-is-now-enabled-again/"
---
標準の [`Array.prototype.values`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/values) メソッド対応が Firefox 60 で再度有効化されました。これは Firefox 48 で実装されましたが、[いくつかの互換性問題](https://www.fxsitecompat.dev/ja/docs/2016/array-prototype-values-breaks-some-legacy-apps/) が報告されたため Nightly チャンネル以外では無効化されていました。

Microsoft Edge と Apple Safari は既にこの機能を提供しています。今年 4 月公開の [Google Chrome 66](https://www.chromestatus.com/feature/4755812090118144) でも再度有効化される予定です。不具合を避けるため、あなたのサイトにこのメソッドの独自実装がないことを確認してください。
