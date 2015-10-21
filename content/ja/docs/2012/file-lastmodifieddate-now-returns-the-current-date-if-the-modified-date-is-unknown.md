---
title: "ファイルの更新日が不明な場合、`File.lastModifiedDate` が現在の日時を返すようになりました"
date: "2012-12-03T03:54:45-05:00"
categories: ["dom"]
tags: []
versions: ["19"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=793459": "Bug 793459 – Update File.lastModifiedDate to latest spec"
---
[File API](http://www.w3.org/TR/FileAPI/) の最新仕様に合わせて、[`File`](https://developer.mozilla.org/ja/docs/DOM/File) オブジェクトの `lastModifiedDate` プロパティが、そのファイルの最終更新日が不明な場合は現在の日時を返すようになりました。従来そうした場合は `null` を返していました。
