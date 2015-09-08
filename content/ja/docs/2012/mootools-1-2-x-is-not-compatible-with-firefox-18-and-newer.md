---
title: "Mootools 1.2.x は Firefox 18 以上と互換性がありません"
date: "2012-12-03T03:53:26-05:00"
categories: ["javascript"]
tags: []
versions: "18"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=789036": "Bug 789036 – Mootools 1.2.x was broken by String.prototype.contains"
---
Firefox 18 では ECMAScript 6 の関数である [`String.prototype.contains`](https://developer.mozilla.org/ja/docs/JavaScript/Reference/Global_Objects/String/contains) が追加されました。残念ながら Mootools の旧バージョンはそのような関数が存在しないことを前提としており、それが存在した場合うまく動作しません。この問題は Mootools 1.3 以上で修正されています。
