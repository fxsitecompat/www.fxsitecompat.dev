---
title: "`-moz-user-select:none` の挙動が `-moz-user-select:-moz-none` や他のブラウザーに統一されました"
date: "2013-02-06T08:44:10-05:00"
categories: ["css"]
tags: []
versions: ["21"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=816298"
      title: "Bug 816298 – Change \"-moz-user-select:none\" to behave like WebKit, IE, and Opera (and \"-moz-user-select:-moz-none\")"
aliases:
    - "/ja/docs/2013/behavior-of-moz-user-select-none-has-been-changed-to-be-consistent-with-moz-user-select-moz-none-and-other-browsers/"
---
従来、[`user-select`](https://developer.mozilla.org/docs/Web/CSS/user-select) プロパティに [`none`](https://developer.mozilla.org/docs/Web/CSS/none) キーワードを指定すると、その要素と子孫要素のテキストが選択不可になり、子孫要素に `-moz-user-select:text` が指定されても選択可能にはなりませんでした。Firefox 21 以降、`none` は `-moz-none` や他のブラウザーと同じような挙動になり、子孫要素上で `-moz-user-select:text` を使うことでテキスト選択を再度有効化できます。
