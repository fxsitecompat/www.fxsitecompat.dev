---
title: "`Map.size`、`Set.size` がプロパティに変わりました"
date: "2012-12-03T03:54:45-05:00"
categories: ["javascript"]
tags: []
versions: ["19"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=807001": "Bug 807001 – Map.prototype.size and Set.prototype.size should be accessor properties"
---
[`Map`](https://developer.mozilla.org/ja/docs/JavaScript/Reference/Global_Objects/Map) オブジェクトに保存されているキーバリューペアの数、[`Set`](https://developer.mozilla.org/ja/docs/JavaScript/Reference/Global_Objects/Set) オブジェクトに保存されている値の数を返す `size` メソッドが読み取り専用プロパティに変更されました。
