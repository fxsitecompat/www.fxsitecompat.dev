---
title: "`document` がアクティブでない場合に `History` オブジェクトが例外投げるようになりました"
date: "2013-12-09T02:32:17-05:00"
categories: ["dom"]
tags: []
versions: ["28"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=940783"
      title: "Bug 940783 – History objects should unconditionally throw if their inner is not current"
---
[`History`](https://developer.mozilla.org/ja/docs/Web/API/History) インターフェイスの仕様が更新され、そのプロパティとメソッドがアクティブでない [`document`](https://developer.mozilla.org/ja/docs/Web/API/document) 上で呼び出された場合に `SecurityError` 例外が投げられるようになりました。これは [`<iframe>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/iframe) 内の [`window.history`](https://developer.mozilla.org/ja/docs/Web/API/window.history) を操作しているようなコードで問題となる可能性があります。
