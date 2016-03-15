---
title: "割り当て済みイベントを初期化しようとしても例外が投げられなくなりました"
date: "2012-12-03T03:50:54-05:00"
categories: ["dom"]
tags: []
versions: ["17"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=768310"
      title: "Bug 768310 – initEvent on already-dispatched event should be a noop (rather than throwing)"
---
[`dispatchEvent`](https://developer.mozilla.org/ja/docs/DOM/element.dispatchEvent) で割り当てられたイベントに対して [`initEvent`](https://developer.mozilla.org/ja/docs/DOM/event.initEvent) を実行すると、従来は例外が投げられていました。他のブラウザと同様に、何もしないという挙動に変更されました。
