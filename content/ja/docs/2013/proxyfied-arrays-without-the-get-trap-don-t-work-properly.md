---
title: "`get` トラップを伴わないプロキシ化配列が正しく動作しません"
date: "2013-02-06T08:44:10-05:00"
categories: ["javascript"]
tags: []
versions: ["21"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=895223": "Bug 895223 – Can\'t JSON stringify a proxy to an array"
---
[`Proxy`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Proxy) オブジェクトは、開発者がオブジェクトを「プロキシ化」することを可能にします。ハンドラ内のトラップはすべてオプションですが、Firefox 21 以降、`get` トラップを伴わないプロキシ化された配列が正しく動作していません。`get` トラップが定義されていない場合、[`Array.length`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/length) が `0` を返し、`set` トラップも呼び出されません。回避策は、コード内で特に必要ない場合でも何もしない `get` トラップを追加することです。

**更新**: この問題は Firefox 40 で修正されました。
