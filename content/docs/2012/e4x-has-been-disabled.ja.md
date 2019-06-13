---
title: "E4X が無効化されました"
date: "2012-12-03T03:50:54-05:00"
categories: ["javascript"]
tags: []
versions: ["17"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=778851"
      title: "Bug 778851 – Turn javascript.options.xml.content off by default"
---
[ECMAScript for XML (E4X)](https://developer.mozilla.org/docs/E4X) は非推奨となり、Firefox 17 で無効化されました。隠し設定 `javascript.options.xml.content` の値を `true` に変更すれば有効になりますが、<del>Firefox 18</del> <ins>Firefox の近い将来のバージョン (当初 Firefox 18 とされていましたが現状未定)</ins> では実装そのものが [完全に削除](https://bugzilla.mozilla.org/show_bug.cgi?id=788293) される予定です。

**更新**: E4X 対応は [Firefox 21 で削除されました](https://www.fxsitecompat.dev/ja/docs/2013/e4x-support-has-been-completely-removed/)。
