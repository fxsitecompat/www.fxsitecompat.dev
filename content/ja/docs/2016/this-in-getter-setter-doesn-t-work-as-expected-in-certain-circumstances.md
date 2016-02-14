---
title: "ゲッター・セッター内の `this` が特定の状況で期待通りに動作しません"
date: "2016-01-02T12:42:00-05:00"
categories: ["javascript"]
tags: []
versions: ["41"]
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1232269": "Bug 1232269 - Getter or setter on unboxed expando object is called with the expando as |this|"
---
[ゲッター・セッター内の `this` キーワード](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this#this_with_a_getter_or_setter) が特定の状況下で当該オブジェクトを参照できず、プロパティアクセス時に予期せぬ `TypeError` につながるというリグレッションが Firefox 41 で発生しました。バグ報告者の例では巨大な配列を含むオブジェクトで問題が生じていましたが、Mozilla 開発者によれば他の条件でも再現する可能性があります。この問題は Firefox 45 で修正されました。
