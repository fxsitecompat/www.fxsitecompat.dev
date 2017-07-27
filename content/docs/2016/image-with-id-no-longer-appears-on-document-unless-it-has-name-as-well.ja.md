---
title: "`id` 付き画像は `name` も指定されていない限り `document` 上に現れなくなりました"
date: "2016-03-10T12:15:00-05:00"
categories: ["dom"]
tags: []
versions: ["45"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1223523"
      title: "Bug 1223523 - Named getter on document should not return images with empty name"
---
従来、`id` 属性付きの画像は常に [`document`](https://developer.mozilla.org/ja/docs/Web/API/Document) 上で使用可能となっており、例えば `<img id="foo">` は `document.foo` でアクセスすることができました。この挙動は仕様に準拠するため変更され、`id` 属性と空白でない `name` 属性が両方指定された画像のみ `document` 上に名前付きプロパティを生成するようになりました。クロスブラウザー互換性を高めるため、常に [`document.getElementById`](https://developer.mozilla.org/ja/docs/Web/API/Document/getElementById) メソッドを代用することが推奨されます。
